pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
        agent {
        docker { image 'espressif/idf' }
      }
      steps {
        sh 'idf.py build'
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