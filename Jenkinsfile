pipeline {
    agent any
    tools {
        maven 'Maven3.5.3'
        jdk 'java1.8.0'
    }
    stages {
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = %PATH%"
                    echo "M2_HOME = %M2_HOME%"
                '''
            }
        }

        stage ('Build') {
            steps {
                    bat 'cd. & mvn install'
            }
             post {
                success {
                    junit 'monappli-domaine/target/surefire-reports/*.xml'
                        }
                 }
               

           
            }
        }
    
}