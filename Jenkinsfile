pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps{
                sh '''
                    ls -la
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}