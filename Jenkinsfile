pipeline {
    agent { label 'master' }
    environment {
        CI = 'true';
    }
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
        stage('test') {
           steps {
                sh 'npm run test'
            }
        }
    }
     post {
        always {
            junit 'output/coverage/junit/junit.xml'
        }
    }
}