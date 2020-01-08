pipeline{
	agent any
	stages{
		stage('POM File'){
			steps{
				withMaven(maven : 'mavenhome'){
					sh 'mvn -f mvnpoject/pom.xml clean install'
				}
			}
		}
		stage('Compile Stage'){
			steps{
				withMaven(maven : 'mavenhome'){
					sh 'mvn -f mvnpoject/pom.xml clean compile'
				}
			}
		}
		stage('Testing Stage'){
			steps{
				withMaven(maven : 'mavenhome'){
					sh 'mvn -f mvnpoject/pom.xml test'
				}
			}
		}
	        stage('Email Notification'){
		mail bcc: '', body: """Hi Team, You build successfully deployed
		                       Job URL : ${env.JOB_URL}
							   Job Name: ${env.JOB_NAME}
Thanks,
DevOps Team""", cc: '', from: '', replyTo: '', subject: "${env.JOB_NAME} Success", to: 'joelmasham@yahoo.com'
		}
   
   }
}
