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

