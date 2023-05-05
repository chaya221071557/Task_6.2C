pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from your version control system
                // e.g., git clone
            }
        }
        stage('Build') {
            steps {
                // Build your code using Maven
                sh 'mvn clean package'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy your packaged code to a server or other destination
                // e.g., scp or rsync
            }
        }
    }
}
