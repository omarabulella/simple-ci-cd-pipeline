pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('checkout'){
            git url:'https://github.com/omarabulella/simple-ci-cd-pipeline'
    }
}

