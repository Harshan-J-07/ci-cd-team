pipeline {
    agent any

    tools {
        nodejs 'Node 18' // Make sure this matches the name in Jenkins -> Global Tool Configuration
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

        stage('Lint') {
            steps {
                sh 'npm run lint' // Make sure package.json has a "lint" script
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build' // Make sure package.json has a "build" script
            }
        }
    }
}