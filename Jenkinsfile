pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the code using a Maven to compile and package of code.'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests to ensure the code functions as expected and integration tests to ensure the different components of the application work together as expected.'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Integrating a code analysis tool to analyze the code and ensure it meets industry standards.'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing a security scan on the code using a tool to identify any vulnerabilities or loopholes in application.'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to a staging server (e.g., AWS EC2 instance).'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on the staging environment to ensure the application functions as expected in a production-like environment.'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying the application to a production server (AWS EC2 instance). Changing to check pipeline'
            }
        }
    }

    post {
        success {
            emailext subject: 'Pipeline Status: SUCCESS',
                body: 'The Jenkins pipeline has successfully completed all stages.',
                to: 's222448467@deakin.edu.au',
                attachLog: true 
        }
        failure {
            emailext subject: 'Pipeline Status: FAILURE',
                body: 'The Jenkins pipeline has failed at one or more stages. Check the logs for details.',
                to: 's222448467@deakin.edu.au',
                attachLog: true 
        }
    }
}
