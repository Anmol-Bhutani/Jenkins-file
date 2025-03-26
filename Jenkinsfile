pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the application using Maven...'
                    echo 'Tool: Maven (for Java builds), npm (for Node.js), or Gradle'
                }
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Running unit and integration tests using JUnit and Selenium...'
                    echo 'Tools: JUnit (Java), PyTest (Python), or Selenium (UI testing)'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                script {
                    echo 'Performing static code analysis using SonarQube...'
                    echo 'Tool: SonarQube or ESLint (for JavaScript), Pylint (for Python)'
                }
            }
        }
        stage('Security Scan') {
            steps {
                script {
                    echo 'Running security scan using OWASP ZAP...'
                    echo 'Tool: OWASP ZAP, Snyk, or Trivy (container security)'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Deploying application to staging server using Docker and Kubernetes...'
                    echo 'Tool: Docker, Kubernetes, or Ansible'
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Running integration tests on staging using Postman or Newman...'
                    echo 'Tool: Postman, Newman, or RestAssured'
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Deploying application to production server using Jenkins and Kubernetes...'
                    echo 'Tool: Jenkins, Docker, Kubernetes, or Ansible'
                }
            }
        }
    }

    post {
        always {
            script {
                echo 'Sending email notification using Jenkins Email Extension Plugin...'
                mail (
                    subject: "Pipeline Notification: ${JOB_NAME} - Build #${BUILD_NUMBER}",
                    body: "The pipeline has completed. Check details at: ${BUILD_URL}",
                    to: 'anmol4762.be23@chitkara.edu.in'
                )
            }
        }
    }
}
