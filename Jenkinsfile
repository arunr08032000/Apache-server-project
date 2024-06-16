pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Pull the latest code
                    git 'https://github.com/KINGNURA007/nginx-server-project.git'

                    // Build Docker image
                    sh 'docker build -t nginx-server .'
                }
            }
        }
    }
} 
