pipeline {
	agent any
	
	stages {
		stage('POM File') {
			steps {
				withMaven(maven : 'mavenhome'){
					sh 'mvn -f mvnproject/pom.xml clean install'
				}
			}
		}

		stage('Compile Stage') {
			steps {
				withMaven(maven : 'mavenhome') {
					sh 'mvn -f mvnproject/pom.xml clean compile'
				}
			}
		}
		
		stage('Testing Stage') {
			steps {
				withMaven(maven : 'mavenhome') {
					sh 'mvn -f mvnproject/pom.xml test'
				}
			}
		}
	   }
    }
