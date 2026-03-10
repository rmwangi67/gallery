pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('Install Dependencies') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }
        stage('Deploy to Render') {
            steps {
                script {
                    sh 'fuser -k 5000/tcp || true'
                    sh 'node server &'
                }
            }
        }
    }
}