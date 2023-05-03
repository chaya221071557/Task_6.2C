pipeline {
    agent any
    tools{
        maven 'maven'
    }
    stages {
        stage('Build') {
            steps {
                withMaven{
                    checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/chaya221071557/Task_6.2C.git']])
                    sh "mvn clean package"
                }
                    
                
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
