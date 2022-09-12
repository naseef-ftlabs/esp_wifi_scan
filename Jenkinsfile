pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh 'cd ~/esp/esp-idf'
        sh 'source export.sh'
        sh 'which idf.py'

         sh 'IDF_PATH="/var/lib/jenkins/esp/esp-idf"'
        sh 'export IDF_PATH'
      }
    }
  }
}