pipeline {
    agent { label 'master' }
    stages {
        stage('build') {
           steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}