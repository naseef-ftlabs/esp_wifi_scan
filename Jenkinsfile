pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh 'echo $IDF_PATH'
        sh '. /var/lib/jenkins/esp/esp-idf/export.sh'
        sh 'which idf.py'

      }
    }
  }
}