pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Munnacs2024/jenkins-test-app.git'
            }
        }
        stage('Build') {
            steps {
                sh 'python -m pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'pytest'
            }
        }
        stage('Deploy') {
            steps {
                sh './deploy.sh' // Replace with your deployment script
            }
        }
    }
}
