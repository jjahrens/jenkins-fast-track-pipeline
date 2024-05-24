pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod a+x run_build_script.sh'
        sh './run_build_script.sh'
      }
    }
    stage('Test') {
      parallel {
        stage('Test On Windows') {
          steps {
            echo "Running tests on Windows Notebook hp ProBook 6570b"
          }
        }
        stage('Test On Linux') {
          steps {
            echo "Running tests on Linux"
          }
        }
      }
    }
  }
}
