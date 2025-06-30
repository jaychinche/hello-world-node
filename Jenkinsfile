pipeline {
    agent any
    
    tools {
        // Make sure this name matches exactly what you configured in Jenkins
        nodejs 'Node17'
    }
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        
        stage('Deploy') {
            steps {
                // Using 'npm start' instead of directly calling node
                sh 'npm start'
            }
        }
    }
}
