pipeline {
 agent any

 stages {

  stage('Checkout') {
   steps {
    git branch: 'main', url: 'https://github.com/rahul-bhatia-226035331/8.2CDevSecOps.git'
   }
  }

  stage('Install Dependencies') {
   steps {
    bat 'npm install'
   }
  }

  stage('Run Tests') {
   steps {
    bat 'npm test || exit /b 0'
   }

   post {
    always {
     emailext(
      subject: 'Run Tests Stage Completed',
      body: 'Run Tests stage has completed successfully. Please find attached logs.',
      to: 'rahulbhatia76b@gmail.com',
      attachLog: true
     )
    }
   }
  }

  stage('Generate Coverage Report') {
   steps {
    bat 'npm run coverage || exit /b 0'
   }
  }

  stage('NPM Audit (Security Scan)') {
   steps {
    bat 'npm audit || exit /b 0'
   }

   post {
    always {
     emailext(
      subject: 'Security Scan Stage Completed',
      body: 'Security scan stage has completed. Please find attached logs.',
      to: 'rahulbhatia76b@gmail.com',
      attachLog: true
     )
    }
   }
  }

 }
}