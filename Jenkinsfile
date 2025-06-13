pipeline {
    agent any
    environment {
      DOCKERHUB_CREDENTIALS = credentials('docker-dockerhub')
    }
    stages {
        stage('Build') {
            steps {
                sh 'sudo docker build -t nginx:latest .'
            }
        }
        stage('Run') {
            steps {
                sh 'sudo docker run -d --name testing -p 8585:80 nginx'
            }
        }
    }
} 
