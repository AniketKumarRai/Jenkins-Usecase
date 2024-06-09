pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            pwsh(script: 'mvn --version', label: 'MavenVersion', returnStatus: true, returnStdout: true)
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