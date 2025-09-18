// Jenkins pipeline with 7 stages and SCM polling every 1 minutes

#comment to observe poll

pipeline {
    agent any
    triggers {
        // Poll GitHub every 1 minutes
        pollSCM('H/1 * * * *')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Stage 1: Build – this stage compiles and packages the code. Common tools used are Maven, Gradle, or npm depending on the technology stack.'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests – this stage runs automated tests. Typical tools include JUnit for Java, Jest for JavaScript, Pytest for Python, and Selenium for integration testing.'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis – this stage performs static code analysis. Tools often used are ESLint for JavaScript, Checkstyle for Java, SpotBugs for bug detection, and SonarQube for overall quality checks.'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan – this stage checks for vulnerabilities in dependencies. Common tools are npm audit, OWASP Dependency Check, and Snyk.'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging – the application is deployed to a staging environment. This is usually done using Docker containers, Kubernetes clusters, or configuration tools like Ansible.'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging – end-to-end and API tests are executed against the staging environment. Tools that can be used include Newman for Postman collections, Cypress for frontend tests, and Selenium for UI tests.'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production – the final deployment step to the production environment. Tools commonly used for this stage are Docker, Kubernetes, and Ansible, often with approval steps for safety.'
            }
        }
    }
}
