pipeline {

  agent any
  stages {

    stage('Checkout') {
      steps {
	checkout scm
        
      }
    }

    stage('Build War File') {
      steps {
	  sh 'export PATH=/var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/maven_jenkins/bin:$PATH'
          sh 'echo mvn -version'
      }
    }
    
    stage('Edit Kube deploy') {
      steps {
	   sh 'sh mod.sh'
      }
    }

    stage('TF Apply') {
      steps {
          sh 'docker images'    
          }
    }

  }

}

