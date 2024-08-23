import groovy.json.JsonSlurper
import groovy.json.JsonSurperClassic

def payload_json = readJSON text: "${payload}"


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
