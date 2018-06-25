pipeline {
  agent {
    node {
      label 'windows'
    }

  }
  stages {
    stage('build') {
      steps {
        ws(dir: 'c:\\\\workspace'){
           bat """
echo %PATH%
PATH=%PATH%;C:\Program Files (x86)\MSBuild\14.0\Bin\
build.cmd
          """
        }
       
      }
    }
  }
}
