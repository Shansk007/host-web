pipeline {
    agent any   // Run on any available agent

    stages {
        stage('Checkout') {
            steps {
                // Pull code from your repository
                git branch: 'main', url: 'https://github.com/Shansk007/host-web.git'
            }
        }

        stage('Build') {
            steps {
                // Example build step
                sh 'echo "Building project..."'
                sh './gradlew build'   // Replace with your build tool (Maven, npm, etc.)
            }
        }

        stage('Test') {
            steps {
                // Run tests
                sh 'echo "Running tests..."'
                sh './gradlew test'
            }
        }

        stage('Deploy') {
            steps {
                // Deployment step (placeholder)
                sh 'echo "Deploying application..."'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check logs.'
        }
    }
}
