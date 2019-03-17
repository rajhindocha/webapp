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
          mvn clean package
          ls -al /var/lib/Jenkins/workspace/test/
      }
    }
    
    stage('Edit Kube deploy') {
      steps {
	sh mod.sh
      }
    }

    stage('TF Apply') {
      steps {
          sh echo 'Done'      
          }
    }

  }

}

