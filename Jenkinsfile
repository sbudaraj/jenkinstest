Jenkinsfile (Declarative Pipeline)

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                    cd /home/ubuntu/WebApp
                    git pull https://github.com/sbudaraj/test
                    sudo docker build -t webapp_flaskapp:latest .
                    echo "All good on western front!"

                '''
            }
        }
        stage('Test') {
            steps {
                sh 'sleep 3'
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                    cd /home/ubuntu/WebApp
                    sudo docker container rm -f webapp_flaskapp_1
                    sudo docker-compose up -d
                    echo "All good on All fronts!"

                '''
            }
        }
    }
}