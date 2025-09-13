// Jenkins pipeline with 7 stages and SCM polling every 1 minutes

pipeline {
    agent any
    triggers {
        // Poll GitHub every 1 minutes
        pollSCM('H/1 * * * *')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Stage 1: Build – compiling and packaging code using Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit tests with JUnit and integration tests with Selenium'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code analysis with SonarQube or Checkstyle'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security scan using OWASP Dependency Check or Snyk'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploying application to staging environment (AWS EC2)'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Running integration tests on staging environment'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploying application to production server (AWS EC2)'
            }
        }
    }
}
