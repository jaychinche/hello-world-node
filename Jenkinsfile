pipeline {
    agent any

    tools {
        nodejs 'Node17' // Make sure this is configured in Jenkins Global Tool Config
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }

    post {
        success {
            echo 'Application Deployed Successfully!'
        }
        failure {
            echo 'Deployment Failed!'
        }
    }
}
