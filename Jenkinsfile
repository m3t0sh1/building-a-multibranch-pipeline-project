pipeline {
    agent {
        docker {
            image 'node:lts-alpine'
            label 'docker-agent'
            args '-p 3000:3000 -p 5050:5050'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'chown -R 997:1002 "/.npm"' 
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}

