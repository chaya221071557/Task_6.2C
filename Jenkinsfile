pipeline {
    agent any
    environment
    {
        PATH="/Maven/apache-maven-3.9.1/bin:$PATH"
       
        
        
    }
    stages {
        stage('Checkout'){
           
            steps{
                 git 'https://github.com/chaya221071557/Task_6.2C.git'
            }
        
        }
        stage('Build') {
            steps {
                
                sh "mvn clean install"
               
                
            }
            
        }
        
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
       
        
        
    }
}
