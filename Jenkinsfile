pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master'
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
                sh 'docker run -d -p 80:80 mysite'
            }
        }
    }
    post {
        always {
            // Add monitoring or logging
        }
    }
}