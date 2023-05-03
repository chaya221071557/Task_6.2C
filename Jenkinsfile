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
                echo "fetch the source code from ${DIRECTORY_PATH}"
                echo "compile the code and generate any necessary artifacts"
                
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
                echo "Deploy the coding application to ${TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                
                sleep 10
                
            }
        }
        stage('Deploy to production') {
            steps {
                echo "Deployment completed by ${PRODUCTION_ENVIRONMENT} using ${TESTING_ENVIRONMENT} environment"
            }
        }
    }
}
