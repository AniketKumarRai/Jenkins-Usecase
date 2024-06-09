pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            bat(script: 'mvn --version', label: 'MAVEN Version', returnStatus: true, returnStdout: true)
          }
        }

        stage('node version') {
          steps {
            powershell(script: 'node -v', label: 'node version', returnStatus: true, returnStdout: true)
          }
        }

      }
    }

  }
}