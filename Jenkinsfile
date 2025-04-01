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
                sh 'npm instal --forcel'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker build -t mi-app .'
                sh 'docker run -d -p 3000:3000 mi-app'
            }
        }
    }

    post {
        success {
            echo '¡Despliegue exitoso!'
        }
        failure {
            echo 'El despliegue falló'
        }
    }
}

