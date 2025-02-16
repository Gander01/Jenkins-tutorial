pipeline {
    agent any

    environment {
        GIT_REPO = 'https://github.com/Gander01/Jenkins-tutorial'
        DOCKER_IMAGE = 'maven:3.9.9-eclipse-temurin-21-alpine'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: "${GIT_REPO}"
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'echo "Building the project..."'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh 'echo "Running tests..."'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh 'echo "Deploying the application..."'
                }
            }
        }
    }
}
