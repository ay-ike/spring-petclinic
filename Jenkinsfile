pipeline {
  agent any
	
	tools{
		maven "MAVEN3"
		jdk "JDK"
	}
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/ay-ike/spring-petclinic', branch: 'main')
      }
    }

  }
}
