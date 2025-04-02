pipeline {
    agent any
    stages {
        stage('Obtener Versiones') {
            steps {
                script {
                    def timestamp = new Date().format("yyyyMMdd_HHmmss")
                    def filename = "versiones_${timestamp}.txt"
                    sh """echo "==== Java Version ====" > ${filename}"""
                    sh "java -version >> ${filename}"
                    sh """echo "==== Jenkins Version ====" >> ${filename}"""
                    sh "java -jar /usr/share/jenkins/jenkins.war --version >> ${filename}"
                }
            }
        }
    }
}

