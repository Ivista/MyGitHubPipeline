import groovy.json.JsonSlurper
import groovy.json.JsonSlurperClassic

def payload_json = readJSON text: "${env.json}"


pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello, World!'
                echo "payload ${payload_json}"
            }
        }
    }
}
