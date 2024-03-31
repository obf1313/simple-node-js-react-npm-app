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
                sh 'npm cache clean -f'
                sh 'npm config set registry https://registry.npm.taobao.org'
                sh 'npm install'
            }
        }
    }
}
