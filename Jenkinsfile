pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            powershell(script: 'mvn --version', returnStatus: true, returnStdout: true, label: 'mvn --version')
            powershell 'mvn --version'
          }
        }

        stage('node version') {
          steps {
            powershell(script: 'node -v', label: 'Node Version', returnStatus: true, returnStdout: true)
          }
        }

      }
    }

  }
}