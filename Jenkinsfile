pipeline {

agent any
triggers { cron('*/5 * * * *') }

    stages {

        stage ('User Confirmation') {
        	steps	{
			input message: 'Proceed or Abort', ok: 'Submit', parameters: [booleanParam(defaultValue: true, description: '', name: '')], submitter: '"Proceed,Abort"', submitterParameter: 'id'
			} }


		stage ('Git Checkout') {
			steps	{
				script {
				try {
					timeout(time: 20, unit: 'SECONDS') {

				checkout([$class: 'GitSCM', branches: [[name: '*/amanjain']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '0c9d8f9a-4556-4f8b-8c37-3393809bbeaa', url: 'https://github.com/Amanjain1612/intellimeet-CICD.git']]])

	  	   		}

				}

				catch(err) {
	                err.printStackTrace()
	                                                }
	                sh 'echo Proceeding'
	               }
	            }
			}
			}
			}

