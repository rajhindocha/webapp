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
          sh echo 'Done'
      }
    }
    
    stage('Edit Kube deploy') {
      steps {
	sh mod.sh
      }
    }

    stage('TF Apply') {
      steps {
          sh mvn -version    
          }
    }

  }

}

