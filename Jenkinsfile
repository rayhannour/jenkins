pipeline {

  
  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/rayhannour/jenkins.git'
      }
    }

    

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "myweb.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
