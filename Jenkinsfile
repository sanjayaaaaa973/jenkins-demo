pipeline {
    agent any

    stages {

        stage('Compile') {
            steps {
                bat 'javac Hello.java'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }

    }
}
