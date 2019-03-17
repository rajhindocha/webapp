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
          sh mvn clean package
          sh ls -al /var/lib/Jenkins/workspace/test/
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

