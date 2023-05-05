pipeline {
    agent any
    
    stages {
        stage('Checkout') 
        {
            steps 
            {
                // Checkout code from your version control system
                // e.g., git clone
                git branch: 'main' , url:'https://github.com/chaya221071557/Task_6.2C.git'
            }
        }
        stage('Build') 
        {
            steps 
            {
                // Build your code using Maven
                echo  "Building project using Maven"
                  
            }
        }
        stage('Unit and Integration Tests')
        {
            steps 
            {
                echo "Unit and Integration Tests working using Maven"
            }
            post
            {
                failure 
                {
                    mail to: 'chayashiv629@gmail.com',
                        subject: "Failure: Unit and Integration Tests",
                        body: "Stage is not working. Please investigate."
                }
                success 
                {
                    mail to: 'chayashiv629@gmail.com',
                        subject: "Success: Unit and Integration Tests",
                        body: "Stage is working. Congratulations!"
                }


            }

        }
        stage('Code Analysis')
        {   
            steps
            {
                 echo 'Performing code analysis using Checkstyle'
            }

        }
        stage('Security Scan')
        {   
            steps 
            {
                echo 'Performing security scan using SonarQube'
            }
            post
            {   


                failure 
                {
                    mail to: 'chayashiv629@gmail.com',
                        subject: "Failure: Security Scan",
                        body: "Stage is not working. Please investigate."
                }
                success 
                {
                    mail to: 'chayashiv629@gmail.com',
                        subject: "Success: Security Scan",
                        body: "Stage is working. Congratulations!"
                }
                


            }
            
        }
        stage('Deploy to Staging')
        {
            steps
            {
                echo 'Deploy to staging sever AWS EC2'

            }
        }
        stage('Integration Tests on Staging')
        {
            steps
            {
                echo 'Run Integration Tests on Staging environment'
            }
        }
        stage('Deploy to Production')
        {
            steps{
                echo'Deploy to Production server AWS EC2'
            }
        }       
        
    }
    post 
    {
        always             
        {

            mail to: 'chayashiv629@gmail.com',
                    subject: "Status: ${currentBuild.result}",
                    body: "Pipeline has been a ${currentBuild.result}."

            
                
        }
    }
}



     
