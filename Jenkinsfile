pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        powershell(script: 'mvn --version', label: 'Maven Version', returnStatus: true, returnStdout: true)
      }
    }

  }
}