pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'rama-cambio-trivial', url: 'https://github.com/EderSaiz/react-redux-eder'
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
            echo 'Ha habido algun error'
        }
    }
}

