pipeline {
    agent {
        docker {
            image 'node:lts-buster-slim'
            args '-p 3001:3001'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm cache clean -f'
                sh 'npm config set registry https://npm.aliyun.com'
                sh 'npm install'
            }
        }
    }
}
