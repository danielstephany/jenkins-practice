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
        stage('test') {
           steps {
                sh 'CI=true npm run test -- --coverage'
            }
        }
    }
    post {
        always {
            junit '**/output/coverage/**/*.xml'
        }
    }
}