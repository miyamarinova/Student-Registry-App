pipeline {
    agent any
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'SECONDS')
    }
    stages {
        stage('NPM Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('NPM Audit') {
            steps {
                sh 'npm audit'
            }
        }
    }
}