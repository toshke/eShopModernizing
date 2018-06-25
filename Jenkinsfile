pipeline {
  agent {
    node {
      label 'windows'
    }

  }
  stages {
    stage('build') {
      steps {
        ws(dir: 'c:\\\\workspace')
        bat 'build.cmd'
      }
    }
  }
}