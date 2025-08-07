pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        bat 'npm install'
      }
    }
    stage('Test') {
      steps {
        bat 'npm test'
      }
    }
    stage('Docker Build') {
      steps {
        bat 'docker build -t simple-node-app .'
      }
    }
    stage('Deploy') {
      steps {
        bat 'echo Deploying app...'
      }
    }
  }
}
