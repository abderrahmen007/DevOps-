pipeline {
    agent any
    environment {
        MY_ENV_VAR = 'value'
    }
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub repository
                git branch: 'main', url: 'https://github.com/abderrahmen007/DevOps-.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Example build step, adjust as necessary
                sh 'echo Build step'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Example test step, adjust as necessary
                sh './run_tests.sh'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Example deploy step, adjust as necessary
                sh './deploy.sh'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}