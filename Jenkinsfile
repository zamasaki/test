pipeline {
  agent any
  stages {
    stage('Checkout Source') {
      steps {
        git url:'https://github.com/zamasaki/test.git', branch:'master'
      }
    }
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "deployment.yml")
        }
      }
    }
  }
}
