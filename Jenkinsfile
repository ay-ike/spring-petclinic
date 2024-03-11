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

  post {
        success {
            jacoco(
                execPattern: '**/build/jacoco/*.exec',
                classPattern: '**/build/classes/java/main',
                sourcePattern: '**/src/main'
            )
        }
    }
}
