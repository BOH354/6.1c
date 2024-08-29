pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the code...'
                    echo 'Task: Compile the code.'
                    echo 'Tool: Maven'
                }
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Running unit and integration tests...'
                    echo 'Task: Run unit tests to ensure the code works as expected.'
                    echo 'Tool: JUnit for unit tests, TestNG for integration tests.'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                script {
                    echo 'Performing code analysis...'
                    echo 'Task: Analyze the code to ensure it meets industry standards.'
                    echo 'Tool: SonarQube'
                }
            }
        }
        stage('Security Scan') {
            steps {
                script {
                    echo 'Performing security scan...'
                    echo 'Task: Identify vulnerabilities in the code.'
                    echo 'Tool: OWASP Dependency Check'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Deploying to staging environment...'
                    echo 'Task: Deploy the application to a staging server.'
                    echo 'Tool: AWS CLI'
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Running integration tests on staging...'
                    echo 'Task: Ensure the application functions as expected in the staging environment.'
                    echo 'Tool: Selenium for UI testing, Postman for API testing'
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Deploying to production...'
                    echo 'Task: Deploy the application to a production server.'
                    echo 'Tool: AWS CLI'
                }
            }
        }
    }

    post {
        success {
            mail to: 'christophergualtieri@outlook.com',
                subject: "Pipeline Success: ${currentBuild.fullDisplayName}",
                body: "The pipeline completed successfully."
    }
}
}
