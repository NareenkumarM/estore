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


pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from the repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Build the Java application using Maven
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                // Run tests using Maven
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application (this step depends on your deployment strategy)
                // Example: Deploy to a Tomcat server
                sh 'cp target/your-app.war /path/to/tomcat/webapps/'
            }
        }
    }
}
