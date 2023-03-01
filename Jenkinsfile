pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                sh 'echo "chackout main"'
                // checkout main
            }
        }
        stage('Build') {
            steps {
                sh '/var/jenkins_home/workspace/reto-devops-pipeline/app'
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
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
