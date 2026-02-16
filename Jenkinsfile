pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/YOUR_USERNAME/YOUR_REPO.git'
            }
        }

        stage('Compile') {
            steps {
                bat 'javac Hello.java'
            }
        }

        stage('Test Run') {
            steps {
                bat 'java Hello'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }
    }

    post {

        success {
            echo 'Build Successful ✅'
        }

        failure {
            echo 'Build Failed ❌'
        }
    }
}
