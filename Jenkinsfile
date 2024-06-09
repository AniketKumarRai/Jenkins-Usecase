pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            powershell(script: 'mvn --version', returnStatus: true, returnStdout: true, label: 'mvn --version')
            powershell(script: 'mvn --version', label: 'mvn --version', returnStatus: true, returnStdout: true)
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