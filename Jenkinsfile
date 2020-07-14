pipeline {
    agent none
    stages {
        stage('Back-end') {
            agent {
                docker { image 'llstrevensll/docker-jenkins-integration-sample' }
            }
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
