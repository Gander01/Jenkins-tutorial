pipeline {
    agent any

    environment {
        // Add any environment variables if needed (like credentials, paths, etc.)
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from GitHub (make sure the repo URL is correct)
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Run Maven to build the project
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests if applicable
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the project (adjust as needed)
                // Example: sh 'mvn deploy'
                echo 'Deploying the project...'
            }
        }
    }

    post {
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
