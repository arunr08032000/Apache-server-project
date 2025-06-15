pipeline {
    agent any
    environment {
      DOCKERHUB_CREDENTIALS = credentials('docker-dockerhub')
    }
    stages {
        stage('Build') {
            steps {
                sh 'sudo docker build -t httpd:latest .'
            }
        }
        stage('Run') {
            steps {
                sh 'sudo docker run -d --name Apache -p 8585:80 httpd'
            }
        }
    }
} 
