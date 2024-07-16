pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('checkout'){
            steps {
                
            git url:'https://github.com/omarabulella/simple-ci-cd-pipeline' , branch: 'main'
    }
            stage('build'){
                steps{
                    sh 'pip install requirements.txt'
                }
            }
            stage('Test'){
                steps{
                sh 'pytest'
                }
            }
            stage('Deploy'){
                steps{
                sh 'docker build -t flas-app . '
                sh 'docker run -d -p 5000:5000 flask-app'
            }}
}
    }
}

