pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				bat 'cd monappli & mvn install'
			}
		 post {
                success {
                    junit 'monappli/monappli-dao/target/surefire-reports/*.xml'
                        }
                 }
               
		}
	}
}