pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from your version control system
                // e.g., git clone
                git branch: 'main' , url:'https://github.com/chaya221071557/Task_6.2C.git'
            }
        }
        stage('Build') {
            steps {
                // Build your code using Maven
                sh 'D:\\Maven\\apache-maven-3.9.1\\bin\\mvn clean package'
            }
        }
        stage('Deploy') {
            steps {
                echo "deploy"
            }
        }
    }
}
