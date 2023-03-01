pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout main
            }
        }
        stage('Build') {
            steps {
                sh 'cd ./app'
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'cd ./app'
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'npm run deploy'
            }
        }
    }
}
