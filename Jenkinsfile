pipeline {

  agent { label 'ba18' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/Alexrubiolv/Playjenkins.git', branch:'main'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
