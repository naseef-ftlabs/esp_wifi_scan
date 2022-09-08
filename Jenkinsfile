pipeline {
  agent none
  stages {
    stage('ESP-IDF Building') {
      agent {
        docker { image 'espressif/idf:release-v4.4' }
      }
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