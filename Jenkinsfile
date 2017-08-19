pipeline {

agent any
triggers { cron('*/5 * * * *') }

    stages {

        stage ('User Confirmation') {
        	steps	{
			input message: 'Proceed or Abort', ok: 'Submit', parameters: [booleanParam(defaultValue: false, description: '', name: '')], submitter: 'Proceed', submitterParameter: 'id'
			} }


			}
			}
			

