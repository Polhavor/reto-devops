pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                sh 'echo "chackout main"'
                sh 'id'
                // checkout main
            }
        }
        stage('Build') {
            steps {
                sh 'cd /var/jenkins_home/workspace/reto-devops-pipeline/app; npm install'
                sh 'cd /var/jenkins_home/workspace/reto-devops-pipeline/app; npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'cd /var/jenkins_home/workspace/reto-devops-pipeline/app; npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'npm run deploy'
            }
        }
    }
}
