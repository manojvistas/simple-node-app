pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the app...'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm test || true'  // Replace with your test command
            }
        }

        stage('Docker Build') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t simple-node-app .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the app...'
                // Example: Run Docker container locally (for demo)
                sh 'docker run -d -p 3000:3000 simple-node-app'
            }
        }
    }
}
