pipeline {
    agent { label 'master' }
    stages {
        stage('build') {
           steps {
                sh 'node --version'
            }
        }
        stage('install') {
           steps {
                sh 'npm install'
            }
        }
        stage('install') {
           steps {
                sh 'npm run test'
            }
        }
    }
}