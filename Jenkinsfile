
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage completed successfully'
            }
        }

        stage('Test') {
            steps {
                echo 'All tests passed successfully'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage completed successfully'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
