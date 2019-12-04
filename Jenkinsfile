pipeline {
  agent any
  stages {
    stage ('Compile')
    steps {
      withMaven (maven : 'mavehome'){
        sh 'maven clean compile'
      }
    }
  }
}
    
