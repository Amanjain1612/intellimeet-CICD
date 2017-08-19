pipeline {

agent any
triggers { cron('*/5 * * * *') }

    stages {

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
		stage("Run Tests") {
        		agent { docker "maven:4-jdk-8" }
            		steps {
				sh 'mvn package'
				sh 'ls -R *'
				withEnv(["PATH+MAVEN=${tool 'maven4'}/bin"]) {
						sh "mvn test"
					}
				}

				}


			}
			}

















		























