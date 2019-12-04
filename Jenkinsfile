pipeline {
  agent any
  stages {
    stage ('Compiling'){
    steps {
      withMaven (maven : 'mavehome'){
        sh 'maven clean compile'
      }
    }
  }
     stage ('Testing'){
    steps {
      withMaven (maven : 'mavehome'){
        sh 'maven test'
      }
    }
  }
     stage ('Deploying'){
    steps {
      withMaven (maven : 'mavehome'){
        sh 'maven Deploying'
      }
    }
  }
 }
}    
