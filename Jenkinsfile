pipeline {
  agent any
  stages {
    stage('pull images') {
      steps {
        sh 'docker pull hashicorp/packer'
      }
    }
  }
}