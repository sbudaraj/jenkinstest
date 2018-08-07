pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t webapp_flaskapp:latest .'
            }
        }
        stage('Test') {
            steps {
                sh 'sleep 3'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}