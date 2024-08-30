pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven...'
                // Example: sh 'mvn clean package'
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests with JUnit...'
                // Example: sh 'mvn test'
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo 'Analyzing code with SonarQube...'
                // Example: sh 'sonar-scanner'
            }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Performing security scan with OWASP Dependency Check...'
                // Example: sh 'dependency-check'
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging Server...'
                // Example: sh 'scp target/myapp.jar user@staging-server:/apps/'
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Integration Tests on Staging...'
                // Example: sh './run-integration-tests.sh'
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production Server...'
                // Example: sh 'scp target/myapp.jar user@production-server:/apps/'
            }
        }
    }
    
    post {
        success {
            mail to: 'developer@example.com',
                 subject: "Pipeline Success",
                 body: "The pipeline has completed successfully."
        }
        failure {
            mail to: 'developer@example.com',
                 subject: "Pipeline Failed",
                 body: "The pipeline has failed. Please check the logs."
        }
    }
}
