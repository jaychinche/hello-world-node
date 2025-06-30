pipeline {
    agent any
    
    tools {
        nodejs 'Node17'  // This must match the name in Global Tool Configuration
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
                sh 'node server.js'  // Adjust to your deploy script
            }
        }
    }
}
