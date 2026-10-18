
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
                bat '"C:\\Program Files\\Python311\\python.exe" src/app.py'
            }
        }

        stage('Test') {
            steps {
                bat '''
                    set "PYTHONPATH=%APPDATA%\\Python\\Python311\\site-packages"
                    "C:\\Program Files\\Python311\\python.exe" -m pytest tests/
                '''
            }
        }

        stage('Deploy') {
            steps {
                bat 'deploy.bat'
            }
        }
    }
}
