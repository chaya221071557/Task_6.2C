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
               
            }
        }
        stage('Approval') {
            steps {
                
                
            }
        }
        stage('Deploy to production') {
            steps {
                
            }
        }
    }
}
