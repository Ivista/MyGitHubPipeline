
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Print the raw JSON payload for debugging
                    echo "Raw Payload: ${env.json}"

                    // Ensure the JSON payload is not empty or null before parsing
                    if (env.json?.trim()) {
                        def jsonSlurper = new groovy.json.JsonSlurper()
                        def payload_json = jsonSlurper.parseText(env.json)
                        echo "Parsed Payload: ${payload_json}"
                    } else {
                        error "Payload is empty or null! Cannot parse JSON."
                    }
                }
            }
        }
    }
}

