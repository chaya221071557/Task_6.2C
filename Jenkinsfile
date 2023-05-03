pipeline {
    agent any
    tools
    {
       
        maven 'maven'
        
    }
    stages {
        stage('Checkout'){
           
            steps{
                 git: 'https://github.com/chaya221071557/Task_6.2C.git'
            }
        
        }
        stage('Build') {
            steps {
                
                sh 'mvn clean package'
               
                
            }
            
        }
        
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
       
        
        
    }
}
