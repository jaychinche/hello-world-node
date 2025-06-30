pipeline {
    agent any

    tools {
        nodejs 'Node17' // Must match the name from Global Tool Configuration
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/jaychinche/hello-world-node.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
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
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
