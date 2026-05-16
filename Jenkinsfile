pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code from GitHub'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test'
            }
        }

        stage('Security Audit') {
            steps {
                bat 'npm audit'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application'
            }
        }

    }
}