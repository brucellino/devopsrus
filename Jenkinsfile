pipeline {
  agent any
  stages {
    stage('pull images') {
      steps {
        sh 'docker pull hashicorp/packer'
        sh 'docker pull nginx'
      }
    stage('Build the images') {
      steps {
        sh 'cd Docker'
        sh 'docker-compose --build'
      }
    }
    }
  }
}