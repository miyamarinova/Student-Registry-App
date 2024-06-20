pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
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