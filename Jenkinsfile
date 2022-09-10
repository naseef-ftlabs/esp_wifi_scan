pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh 'echo "jenkins" | sudo -S su ftlabs && ./home/ftlabs/esp/esp-idf/export.sh'
        sh 'echo "jenkins" | sudo -S su ftlabs && /home/ftlabs/esp/esp-idf/tools/idf.py build'
      }
    }
  }
}