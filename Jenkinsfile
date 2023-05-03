pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mv clean package'
                
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
