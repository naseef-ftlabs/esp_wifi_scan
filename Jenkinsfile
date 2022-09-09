pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      agent {
        docker { image 'espressif/esp32-ci-env' }
      }
      steps {
        sh 'idf.py build'
      }
    }
  }
  post {
  always {
    cleanWs()
  }
}
}