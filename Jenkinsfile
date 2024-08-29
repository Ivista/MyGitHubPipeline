
// pipeline {
//     agent any

//     stages {
//         stage('Build') {
//             steps {
//                 script {
//                     // Print the raw JSON payload for debugging
//                     echo "Raw Payload: ${env.json}"

//                     // Ensure the JSON payload is not empty or null before parsing
//                     if (env.json?.trim()) {
//                         def jsonSlurper = new groovy.json.JsonSlurper()
//                         def payload_json = jsonSlurper.parseText(env.json)
//                         echo "Parsed Payload: ${payload_json}"
//                     } else {
//                         error "Payload is empty or null! Cannot parse JSON."
//                     }
//                 }
//             }
//         }
//     }
// }

import groovy.json.JsonSlurper
import groovy.json.JsonOutput

pipeline {
    agent any

    stages {
        stage('Display Pretty JSON') {
            steps {
                script {
                    // Check if the JSON payload is not empty
                    if (env.json?.trim()) {
                        // Parse the JSON payload
                        def jsonSlurper = new JsonSlurper()
                        def payloadJson = jsonSlurper.parseText(env.json)
                        
                        // Convert and pretty-print the JSON
                        def prettyJson = JsonOutput.prettyPrint(JsonOutput.toJson(payloadJson))
                        
                        // Display the pretty-printed JSON in the console
                        echo "Formatted JSON Payload:\n${prettyJson}"
                    } else {
                        error "Payload is empty or null! Cannot parse JSON."
                    }
                }
            }
        }
    }
}


