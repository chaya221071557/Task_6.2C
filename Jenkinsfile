pipeline {
    agent any

    tools {
        maven "maven"
    }

    stages {
        stage('Initialize'){
            steps{
                git branch: 'main', url: 'https://github.com/chaya221071557/Task_6.2C.git'
                sh 'maven clean package'
            }
        }
        stage('Build') {
            steps {
                echo"print"
            }
            
        }
        
     }
    
}
