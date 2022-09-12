pipeline {
  agent any
  stages {
    stage('ESP-IDF Building') {
      steps {
        sh 'export IDF_PATH=/var/lib/jenkins/esp/esp-idf'
        sh '. /var/lib/jenkins/esp/esp-idf/tools/detect_python.sh'
        sh 'which python'
        sh'"$ESP_PYTHON" "${IDF_PATH}/tools/python_version_checker.py"'

        sh 'export IDF_TOOLS_EXPORT_CMD=${IDF_PATH}/export.sh'
        sh 'export IDF_TOOLS_INSTALL_CMD=${IDF_PATH}/install.sh'
        sh 'IDF_ADD_PATHS_EXTRAS="${IDF_PATH}/components/esptool_py/esptool"'
        sh 'IDF_ADD_PATHS_EXTRAS="${IDF_ADD_PATHS_EXTRAS}:${IDF_PATH}/components/espcoredump"'
        sh 'IDF_ADD_PATHS_EXTRAS="${IDF_ADD_PATHS_EXTRAS}:${IDF_PATH}/components/partition_table"'
        sh ' IDF_ADD_PATHS_EXTRAS="${IDF_ADD_PATHS_EXTRAS}:${IDF_PATH}/components/app_update"'
      }
    }
  }
}