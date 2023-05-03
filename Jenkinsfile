pipeline {
    agent any
    
    stages {
        stage('Checkout'){
            git 'https://github.com/chaya221071557/Task_6.2C.git'
        
        }
        stage('Build') {
            steps {
                sh 'mvn package'
                
            }
            
        }
        
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
       
        
        
    }
}
