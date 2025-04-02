pipeline {
    agent any
    stages {
        stage('Escaneo de Puertos') {
	    steps {
		script {
		    def timestamp = new Date().format("yyyyMMdd_HHmmss")
		    def filename = "hashes_${timestamp}.txt"
		    sh """echo "==== Hashes de los dos ficheros anteriores ====" > ${filename}"""
		    sh "find /var/jenkins_home/workspace/Feature-CI-Pipeline/versiones_20250402_103217.txt -type f -exec sha256sum {} + >> ${filename}"
		    sh "find /var/jenkins_home/workspace/Feature-CI-Pipeline/puertos_20250402_105418.txt -type f -exec sha256sum {} + >> ${filename}"
		}
	    }
	}
    }
}
