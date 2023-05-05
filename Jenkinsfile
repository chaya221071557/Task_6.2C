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
                success
                {
                    def email_address='chayashiv629@gmail.com'
                    def email_subject='Sucess: Unit and Integration Tests'
                    def email_body='Stage is working'
                    println "Email sent to: ${email_address}"
                    println "Email subject: ${email_subject}"
                    println "Email body: ${email_body}"
                    emailext(
                        to: email_address,
                        subject: email_subject,
                        body: email_body,
                        mimeType: 'text/html',
                        attachLog: true
                    
                        
                    )

                }
                failure
                {
                    def email_address='chayashiv629@gmail.com'
                    def email_subject='Failure: Unit and Integration Tests'
                    def email_body='Stage is not working'
                    println "Email sent to: ${email_address}"
                    println "Email subject: ${email_subject}"
                    println "Email body: ${email_body}"
                    emailext{
                        to: email_address,
                        subject: email_subject,
                        body: email_body,
                        mimeType: 'text/html',
                        attachLog: true
                    
                        
                    }

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
                success
                {
                    def email_address='chayashiv629@gmail.com'
                    def email_subject='Success: Security Scan'
                    def email_body='Stage is working'
                    println "Email sent to: ${email_address}"
                    println "Email subject: ${email_subject}"
                    println "Email body: ${email_body}"
                    emailext(
                        to: email_address,
                        subject: email_subject,
                        body: email_body,
                        mimeType: 'text/html',
                        attachLog: true
                    
                        
                    )

                }
                failure
                {
                    def email_address='chayashiv629@gmail.com'
                    def email_subject='Failure: Security Scan'
                    def email_body='Stage is not working'
                    println "Email sent to: ${email_address}"
                    println "Email subject: ${email_subject}"
                    println "Email body: ${email_body}"
                    emailext{
                        to: email_address,
                        subject: email_subject,
                        body: email_body,
                        mimeType: 'text/html',
                        attachLog: true
                    
                        
                    }

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
            def email_address='chayashiv629@gmail.com'
            def email_subject='Status: ${currentBuild.result}'
            def email_body='Pipeline has been a ${currentBuild.result}'                
            println "Email sent to: ${email_address}"
            println "Email subject: ${email_subject}"
            println "Email body: ${email_body}"
            emailext
            {
                to: email_address,
                subject: email_subject,                        
                body: email_body,
                mimeType: 'text/html',
                attachLog: true
                    
                        
            }
                
        }
    }
}



     
