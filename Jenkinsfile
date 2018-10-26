pipeline {
    agent any 
    stages {
        stage('clone repo and clean') { 
            steps {
                bat "rmdir /s /q pipelinetest"
                bat "git clone https://github.com/ericmaonc/pipelinetest.git"
                bat "mvn clean -f pipelinetest"
            }
        }
        stage('Test') { 
            steps {
                bat "mvn test -f pipelinetest"
            }
        }
        stage('Deploy') { 
            steps {
                bat "mvn package -f pipelinetest" 
            }
        }
    }
}