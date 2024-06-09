pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            powershell 'mvn --version'
            powershell(script: 'mvn --version', label: 'Maven Version', returnStatus: true, returnStdout: true)
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