pipeline {
    agent {
        docker {
            image 'node:lts-alpine'
            label 'docker-slave'
            args '-p 3000:3000 -p 5050:5050'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
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

