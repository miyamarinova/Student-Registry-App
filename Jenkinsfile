pipeline {
    agent any
     tools {
        nodejs "nodejs-lts" // name of NodeJS installation in Jenkins
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
        stage('Run integration tests') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                script{
                    input message: 'Approve deployment?', ok: 'Deploy'
                }
                echo 'Deploying'
            }
        }
        }
       
    }
