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
          sh 'sudo mvn -version'
      }
    }
    
    stage('Edit Kube deploy') {
      steps {
	   sh 'sudo sh mod.sh'
      }
    }

    stage('TF Apply') {
      steps {
          sh 'sudo docker images'    
          }
    }

  }

}

