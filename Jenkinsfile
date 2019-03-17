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
	   sh 'sh mod.sh'
      }
    }

    stage('TF Apply') {
      steps {
          sh 'sudo docker images'    
          }
    }

  }

}

