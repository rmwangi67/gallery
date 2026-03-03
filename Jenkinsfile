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
                    sh 'node server'
                }
            }
        }
    }
}