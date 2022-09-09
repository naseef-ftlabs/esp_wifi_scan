pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      agent {
        docker { image 'espressif/idf:v4.3.3' }
      }
      steps {
        sh 'idf.py build'
      }
    }
  }
  post {
  always {
    cleanWs()
    dir("${env.WORKSPACE}@tmp") {
      deleteDir()
    }
    dir("${env.WORKSPACE}@script") {
      deleteDir()
    }
    dir("${env.WORKSPACE}@script@tmp") {
      deleteDir()
    }
  }
}
}