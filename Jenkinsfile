pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
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