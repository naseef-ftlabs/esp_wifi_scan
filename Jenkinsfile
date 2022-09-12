pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh 'export IDF_PATH=/var/lib/jenkins/esp/esp-idf'
        sh '. /var/lib/jenkins/esp/esp-idf/tools/detect_python.sh'
        sh 'which python3'
        sh 'alias python=python3'
        sh 'python3 /var/lib/jenkins/esp/esp-idf/tools/python_version_checker.py'

        sh 'cd ~'
        sh '. /var/lib/jenkins/esp/esp-idf/export.sh'
        sh 'which idf.py'
      }
    }
  }
}