pipeline {
  agent any
  stages {
    stage('Sanity check') {
      parallel {
        stage('Sanity check') {
          steps {
            sh 'echo "hi"'
            sh 'echo "this is step two"'
          }
        }
        stage('Another sanity check') {
          steps {
            sh 'echo "is anybody out there?"'
          }
        }
      }
    }
    stage('Build') {
      steps {
        sh 'echo "building"'
        sleep 3
      }
    }
  }
}