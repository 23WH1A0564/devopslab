pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Checking out code from Git..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
                // Example: sh 'mvn clean install'  // Uncomment for Maven builds
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                // Example: sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying the project..."
                // Example: sh './deploy.sh'
            }
        }
    }
}

