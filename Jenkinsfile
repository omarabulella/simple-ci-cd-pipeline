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
       
}
    }


