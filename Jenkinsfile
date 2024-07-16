pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                  git 'https://github.com/omarabulella/simple-ci-cd-pipeline'

            }
        }

        stage('Build') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker build -t flask-app .'
                sh 'docker run -d -p 5000:5000 flask-app'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}

