pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            powershell 'mvn --version'
          }
        }

        stage('node version') {
          steps {
            powershell(script: 'node -v', returnStdout: true, returnStatus: true, label: 'node')
          }
        }

      }
    }

  }
}