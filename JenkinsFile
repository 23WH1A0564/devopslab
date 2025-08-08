pipeline {
    agent any

    environment {
        // Define environment variables if needed, e.g.:
        // DEPLOY_SERVER = "user@yourserver.com"
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout your Git repository
                git branch: 'main', url: 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Example build commands:
                // sh 'mvn clean package'         // for Java/Maven
                // sh 'npm install && npm run build' // for Node.js
                // sh './build.sh'                // your custom script
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Example test commands:
                // sh 'mvn test'
                // sh 'npm test'
                // sh './run-tests.sh'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Example deploy steps (customize as needed):
                // sh 'scp target/app.jar user@server:/path/to/deploy'
                // sh 'ssh user@server "systemctl restart myapp"'
                // Or trigger a container deploy, Kubernetes rollout, etc.
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
            // Add notifications here if needed (email, Slack, etc.)
        }
        failure {
            echo 'Pipeline failed!'
            // Notifications on failure if desired
        }
    }
}
