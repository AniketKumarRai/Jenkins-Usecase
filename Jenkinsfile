pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            powershell(script: 'mvn --version', label: 'Maven Version', returnStatus: true, returnStdout: true)
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