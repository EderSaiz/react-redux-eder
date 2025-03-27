pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'feature', url: 'https://github.com/tu-usuario/tu-repo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        success {
            echo 'Build y pruebas exitosas'
        }
        failure {
            echo 'Algo falló'
        }
    }
}
