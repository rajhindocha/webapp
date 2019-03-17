pipeline {

  agent any
  stages {

    stage('Checkout') {
      steps {
	checkout scm
        sh 'export PATH=/var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/maven_jenkins/bin:$PATH'
      }
    }

    stage('Build War File') {
      steps {
          sh 'echo $pwd'
      }
    }
    
    stage('Edit Kube deploy') {
      steps {
	   sh 'mvn -version'
	   sh 'sudo sh /home/opc/mod.sh'
      }
    }

    stage('TF Apply') {
      steps {
          sh 'mvn -version'    
          }
    }

  }

}

