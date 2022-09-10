pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh '. /home/ftlabs/esp/esp-idf/export.sh'
        sh '/home/ftlabs/esp/esp-idf/tools/idf.py build'
      }
    }
  }
}