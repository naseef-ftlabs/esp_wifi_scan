pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh 'pwd && ./idf.py build'
      }
    }
  }
}