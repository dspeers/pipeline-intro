pipeline {
  agent {
    docker {
      image 'maven:alpine'
    }
    
  }
  libraries {
    lib("SharedLibs")
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -v '
	sh 'date'
      }
    }
    stage('Shared Lib') {
         steps {
             helloWorld("Jenkins")
         }
      }
  }
}
