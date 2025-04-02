pipeline {
    agent any
    stages {
        stage('Obtener Versiones') {
            steps {
                script {
                    def timestamp = new Date().format("yyyyMMdd_HHmmss")
                    def filename = "versiones_${timestamp}.txt"
                    sh "java -version > ${filename} 2>&1"
                    sh "jenkins --version >> ${filename}"
                }
            }
        }
    }
}

