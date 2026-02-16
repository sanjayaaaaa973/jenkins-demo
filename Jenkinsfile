pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code checked out from Git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

    }

    post {

        success {
            echo 'Build completed successfully!'
        }

        failure {
            echo 'Build failed. Please check logs.'
        }
