pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t mysite .'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing..."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying..."'
            }
        }
    }
    post {
        always {
            // Add monitoring or logging
        }
    }
}