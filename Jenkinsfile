pipeline {
    agent any

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
        stage('Run integration tests') {
            steps {
                sh 'npm test'
            }
        }
        }
       
    }
