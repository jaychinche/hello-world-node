pipeline {
    agent any
    
    stages {
        stage('Test Jenkins') {
            steps {
                echo "✅ Jenkins is working!"
                sh 'echo "System Info:" && uname -a'
                sh 'echo "Java Version:" && java -version'
                sh 'echo "Jenkins Workspace:" && pwd'
            }
        }
    }
    
    post {
        always {
            echo "🚀 Pipeline execution completed"
        }
    }
}
