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
<<<<<<< HEAD
=======
        stage('Build') {
            steps {
                sh 'chown -R 997:1002 "/.npm"' 
                sh 'npm install'
            }
        }
>>>>>>> parent of 69e03bd (Add initial Jenkinsfile with 'Test' stage)
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}

