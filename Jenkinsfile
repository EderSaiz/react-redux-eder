pipeline {
    agent any
    stages {
        stage('Obtener Versiones') {
            steps {
                script {
                    def timestamp = new Date().format("yyyyMMdd_HHmmss")
                    def filename = "versiones_${timestamp}.txt"
                    sh """
                        echo "==== Java Version ====" > ${filename}
                        java -version 2>&1 | tee -a ${filename}
                        echo "\\n==== Jenkins Version ====" >> ${filename}
                        java -jar /usr/share/jenkins/jenkins.war >> ${filename}" >> ${filename}
                    """
                }
            }
        }
    }
}


