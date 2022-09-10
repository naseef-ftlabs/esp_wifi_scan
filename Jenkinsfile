pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh 'cd /var/lib/jenkins/workspace/'
        sh 'pwd && ./idf.py build'
      }
    }
  }
}