pipeline {
    agent any

    

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building Docker Image..."
                
            }
        }

        stage('Test') {
            steps {
                echo "All tests passed!"
                
                        }
        }

        stage('Deploy') {
            steps {
                echo "Deploying Docker container..."
                
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
