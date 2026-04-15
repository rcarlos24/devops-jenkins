pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/rcarlos24/devops-jenkins.git'
            }
        }
        
        stage('Run Script') {
            steps {
                bat 'app.bat'
            }
        }
        
    }
    
    post {
        success {
            echo 'Pipeline ejecutado correctamente'
        }
        failure {
            echo 'Algo fallo'
        }
    }
}