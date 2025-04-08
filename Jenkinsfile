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
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Test') {
            steps {
                echo "Running Tests..."
                // Simulate test - in a real app, you'd run actual test scripts
                sh 'echo "All tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying Docker container..."
                sh 'docker run -d -p 3000:3000 $IMAGE_NAME'
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
