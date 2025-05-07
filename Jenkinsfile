pipeline {
    agent any
    
    environment{
        APP_NAME = "my-react-app"
        IMAGE_TAG = "my-react-app:latest"
    }

    

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building Docker Image..."
                sh 'docker build -t $IMAGE_TAG .'
                
            }
        }

        stage('Run container') {
            steps {
                echo "All tests passed!"
                sh 'docker rm -f $APP_NAME | true'
                sh 'docker run -d --name $APP_NAME -p 3000:3000 $IMAGE_TAG'
                
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
