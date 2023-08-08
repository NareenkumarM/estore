pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from the repository
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install Node.js and npm
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                // Build the Angular application
                sh 'ng build --prod'
            }
        }

        stage('Deploy to AWS') {
            steps {
                // Deploy the built application to AWS or your desired platform
                // Example: Upload the build artifacts to an S3 bucket
                sh 'aws s3 sync dist/ s3://your-s3-bucket-name'
            }
        }
    }
}
