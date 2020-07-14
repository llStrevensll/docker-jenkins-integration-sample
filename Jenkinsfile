pipeline {
    agent any
    stages {
	stage('Build') {
	    steps {
       	        sh "mvn clean install"
	    }
	}
	stage('Back-end') {
            agent { dockerfile true }
            steps {
		echo 'Backend-Maven'
                sh 'mvn --version'
            }
        }
        stage('Front-end') {
            steps {
		echo 'Frontend-Angular'
                sh 'node --version'
            }
        }
    }
}
