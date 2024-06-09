pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat(script: 'mvn --version', label: 'MAVEN Version', returnStatus: true, returnStdout: true)
      }
    }

  }
}