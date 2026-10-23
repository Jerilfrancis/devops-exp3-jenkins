
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Code retrieved from GitHub'
            }
        }
        stage('Test') {
            steps {
                bat 'if exist index.html (exit /b 0) else (exit /b 1)'
                echo 'Test passed'
            }
        }
        stage('Build') {
            steps {
                bat 'if not exist build mkdir build'
                bat 'copy /Y index.html build\\index.html'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment completed'
            }
        }
    }
}
