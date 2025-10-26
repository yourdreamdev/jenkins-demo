pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub...'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Run App') {
            steps {
                sh 'node index.js'
            }
        }
    }

    post {
        success {
            echo '✅ Build successful!'
        }
        failure {
            echo '❌ Build failed!'
        }
    }
}
