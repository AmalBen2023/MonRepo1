pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				bat 'mvn install'
			}
		 post {
                success {
                    junit 'monappli/monappli-domaine/target/surefire-reports/*.xml'
                        }
                 }
               
		}
	}
}