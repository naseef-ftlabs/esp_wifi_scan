pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh 'export IDF_PATH="/var/lib/jenkins/esp/esp-idf"'
        sh 'echo $IDF_PATH'
        sh 'cd ~/esp/esp-idf'
        sh '. /var/lib/jenkins/esp/esp-idf/export.sh'
        sh 'which idf.py'
      }
    }
  }
}