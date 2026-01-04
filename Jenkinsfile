pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('install dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('run tests') {
            steps { 
                bat 'npm test'
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
