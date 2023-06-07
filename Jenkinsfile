
pipeline {
    agent any 
    options {
        ansiColor('xterm')
    }
    environment {
        MAVEN_OPTS = '-Djansi.force=true'
        ENVIRONMENT = 'staging'																		
    }

    stages {

        stage('Deploy API') { 
		steps {
		        withCredentials([steps.usernamePassword(
				credentialsId: 'STAGING_APIM',
				usernameVariable: 'APIM_USER_STAGING',
				passwordVariable: 'APIM_PWD_STAGING')])
				{ 
				     sh './gradlew deployAPI'
				}
            }
        }

	 stage('Cleanup') { 
            steps {
                step([$class: 'WsCleanup'])
            }
        }
    }
}
