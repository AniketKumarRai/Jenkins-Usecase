pipeline {
  agent any
  stages {
    stage('Builds') {
      parallel {
        stage('Maven Version') {
          steps {
            powershell 'mvn --version'
          }
        }

        stage('node version') {
          steps {
            powershell 'node -v'
          }
        }

      }
    }

    stage('Build') {
      steps {
        powershell 'mvn clean compile test package'
      }
    }

  }
}