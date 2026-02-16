pipeline {
    agent any

    stages {

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
