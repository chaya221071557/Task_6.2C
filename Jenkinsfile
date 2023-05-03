pipeline {
    agent any
     environment{
        DIRECTORY_PATH="\\Users\\Administrator\\Downloads\\SIT223_Task5.1P"
        TESTING_ENVIRONMENT="Jenkins"
        PRODUCTION_ENVIRONMENT="Chaya"
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
                
            }
            
        }
        stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
                
            }
            
        }
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "a"
               
            }
        }
        stage('Approval') {
            steps {
                echo "a"
                
            }
        }
        stage('Deploy to production') {
            steps {
                echo "a"
            }
        }
    }
}
