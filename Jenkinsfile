pipeline {
    agent any
    stages {
        stage('Escaneo de Puertos') {
	    steps {
		script {
		    def timestamp = new Date().format("yyyyMMdd_HHmmss")
		    def filename = "puertos_${timestamp}.txt"
		    sh "nmap -p- 127.0.0.1 > ${filename}"
		}
	    }
	}
    }
}
