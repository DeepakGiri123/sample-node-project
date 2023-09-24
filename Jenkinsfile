pipeline {
    agent any
    environment {
        // Use the NODE_PATH global environment variable to set Node.js and npm paths
        PATH = "${NODE_PATH}:${PATH}"
    }
    stages {       
        stage('Build') {
            steps {
                // Build the Node.js application
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                // Run unit tests
                sh 'npm test'
            }
        }
    }
    post {
        success {
            // Trigger additional actions on pipeline success
            echo 'Build and test passed!'
        }
        failure {
            // Handle pipeline failure
            echo 'Build or test failed!'
        }
    }
}
