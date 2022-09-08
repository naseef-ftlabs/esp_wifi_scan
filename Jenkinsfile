pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
        steps {
            sh 'idf.py build'
        }
    }
    stage('Testing') {
      agent {
        docker { image 'throwtheswitch/madsciencelab' }
      }
      steps {
        sh 'ceedling'
      }
    }
  }
}