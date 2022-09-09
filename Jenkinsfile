pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      agent {
        docker { image 'espressif/idf:latest' }
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