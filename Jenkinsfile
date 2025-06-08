pipeline {
    agent any

    tools {
        nodejs 'nodejs22' // Make sure this matches the name in Jenkins -> Global Tool Configuration
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Harshan-1-a7/ci-cd-team.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Test does here"'
            }
        }

        stage('Run App') {
            steps {
                sh 'node server.js & sleep 5'
            }
        }
    }
}