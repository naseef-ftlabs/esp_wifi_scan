pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      agent {
        docker { image 'espressif/idf:release-v4.3' }
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