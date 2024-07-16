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
    }}
            stage('build'){
                steps{
                    sh 'pip install -r requirements.txt'
                }
            }
        stage('test'){
            steps{
                sh 'pytest'
            }
        }
        
        stage('Deploy'){
            steps{
            sh 'docker build -t flask-app'
            sh 'docker run -d -p 5000:5000 flask-app'
            }
        }
       
}
    }


