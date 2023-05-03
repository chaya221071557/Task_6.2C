pipeline {
    agent any
    tools
    {
        tool name: 'maven', type: 'maven'
        maven 'maven'
        
    }
    stages {
        stage('Checkout'){
           
            steps{
                 git 'https://github.com/chaya221071557/Task_6.2C.git'
            }
        
        }
        stage('Build') {
            steps {
                
                sh '${mvnHome}/bin/mvn package'
                echo "Hello"
                
            }
            
        }
        
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
       
        
        
    }
}
