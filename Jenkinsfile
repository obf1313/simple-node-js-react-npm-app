pipeline {
    agent {
        docker {
            image 'node:lts-buster-slim'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm remove node_modules'
                sh 'npm remove package-lock.json'
                sh 'npm install'
            }
        }
    }
}
