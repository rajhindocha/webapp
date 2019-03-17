pipeline {

  agent any
  stages {

    stage('Checkout') {
      steps {
	checkout scm
        
      }
    }

    stage('Maven Build') {
      steps {
	  sh 'sh maven_build.sh'
      }
    }
    
    stage('Add docker layer') {
      steps {
	   sh 'sh add_docker_layer.sh'
      }
    }

    stage('Push to OCIR') {
      steps {
          sh 'sh ocir_push.sh'    
          }
    }
	  
    stage('OKE Deploy') {
      steps {
          sh 'sh kube_deploy.sh'    
          }
    }

  }

}

