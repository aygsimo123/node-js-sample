pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps { checkout scm }
    }

    stage('Install dependencies') {
      steps { bat 'npm install' }
    }

    stage('Show scripts') {
      steps { bat 'npm run' }
    }

    // À remplacer selon ce que "npm run" affiche
    stage('Build or Start') {
      steps { bat 'npm run build' }
    }
  }
}
