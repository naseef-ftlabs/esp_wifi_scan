pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh 'echo $IDF_PATH'
        sh 'cd ~/esp/esp-idf'
        sh 'pwd'
        sh 'printenv'
        sh '. /var/lib/jenkins/esp/esp-idf/install.sh'
        sh '. /var/lib/jenkins/esp/esp-idf/export.sh'
        sh 'which idf.py'

         sh 'IDF_PATH="/var/lib/jenkins/esp/esp-idf"'
        sh 'export IDF_PATH'
      }
    }
  }
}