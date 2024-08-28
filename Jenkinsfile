pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Parse the JSON payload
                    def jsonSlurper = new groovy.json.JsonSlurper()
                    def payload_json = jsonSlurper.parseText(env.json)

                    // Print a message to the console
                    echo 'Hello, World!'
                    echo "Parsed Payload: ${payload_json}"

                    // You can access specific parts of the payload like this:
                    // if (payload_json.pull_request && payload_json.pull_request.merged) {
                    //     echo "Pull request has been merged into ${payload_json.pull_request.base.ref}."
                    // } else if (payload_json.head_commit && payload_json.head_commit.message.contains("Merge")) {
                    //     echo "A merge has been detected in the latest commit to ${payload_json.ref}."
                    // } else {
                    //     echo "No merge detected."
                    }
                }
            }
        }
    }
