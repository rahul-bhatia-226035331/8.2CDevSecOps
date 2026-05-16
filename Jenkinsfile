pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Build Stage'
                echo 'Tools Used: Maven, Gradle'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests'
                echo 'Tools Used: JUnit, Selenium'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis'
                echo 'Tools Used: SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing security scan'
                echo 'Tools Used: OWASP Dependency-Check, Snyk'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying application to staging environment'
                echo 'Tools Used: Docker, Kubernetes'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging'
                echo 'Tools Used: Postman'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying application to production environment'
                echo 'Tools Used: AWS, Kubernetes'
            }
        }
    }
}