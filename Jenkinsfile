pipeline{
	agent any
	stages{
		stage('POM File'){
			steps{
				withMaven(maven : 'mavenhome'){
					sh 'mvn -f MvnDemo/pom.xml clean install'
				}
			}
		}
		stage('Compile Stage'){
			steps{
				withMaven(maven : 'mavenhome'){
					sh 'mvn -f MvnDemo/pom.xml clean compile'
				}
			}
		}
		stage('Testing Stage'){
			steps{
				withMaven(maven : 'mavenhome'){
					sh 'mvn -f MvnDemo/pom.xml test'
				}
			}
		}
		stage('Deployment Stage'){
			steps{
				withMaven(maven : 'mavenhome'){
					sh 'mvn -f MvnDemo/pom.xml deploy'
				}
			}
		}
	}
}
