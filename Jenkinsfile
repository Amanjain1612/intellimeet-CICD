pipeline {

agent any
triggers { cron('*/5 * * * *') }

    stages {

        stage ('User Confirmation') {
        	steps	{
			input message: 'Proceed or Abort', ok: 'Submit', parameters: [booleanParam(defaultValue: true, description: '', name: '')], submitter: '"Proceed,Abort"', submitterParameter: 'id'
			} }


			}
			}
			

