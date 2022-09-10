pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh 'echo "ftlabs" | sudo -S su ftlabs && ./home/ftlabs/esp/esp-idf/export.sh'
        sh 'echo "ftlabs" | sudo -S su ftlabs && /home/ftlabs/esp/esp-idf/tools/idf.py build'
      }
    }
  }
}