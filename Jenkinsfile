pipeline {
    agent any
    stages {
        stage('Comparación de Estados') {
	    steps {
		script {
		    sh "diff versiones_20250402_103217.txt versiones_actuales.txt > diferencias_versiones.txt || true"
		    sh "diff puertos_20250402_105418.txt puertos_actuales.txt > diferencias_puertos.txt || true"
		    sh "diff hashes_20250402_110639.txt hashes_actuales.txt > diferencias_hashes.txt || true"
		}
	    }
	}
    }
}
