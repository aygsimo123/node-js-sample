pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run tests') {
            steps {
                bat 'npm run'
            }
        }
    }

    post {
        success {
            echo '✅ Tests passed successfully'
        }
        failure {
            echo '❌ Tests failed'
        }
    }
}
