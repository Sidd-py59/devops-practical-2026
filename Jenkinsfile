
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Sidd-py59/devops-practical-2026.git'
            }
        }

        stage('Build') {
            steps {
                bat 'python src/app.py'
            }
        }

        stage('Test') {
            steps {
                bat 'python -m pytest tests/'
            }
        }

        stage('Deploy') {
            steps {
                bat 'deploy.bat'
            }
        }
    }
}
