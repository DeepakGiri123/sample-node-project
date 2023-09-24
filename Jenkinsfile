pipeline {
    agent any
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
