pipeline {
  agent {
    node {
      label 'windows'
    }

  }
  stages {
    stage('build') {
      steps {
        bat(script: 'build.cmd', returnStdout: true, returnStatus: true)
      }
    }
  }
}