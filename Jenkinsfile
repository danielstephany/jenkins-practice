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
            step([$class: 'CoberturaPublisher', coberturaReportFile: 'output/coverage/jest/cobertura-coverage.xml'])
        }
    }
}