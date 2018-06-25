pipeline {
  agent {
    node {
      label 'windows'
      customWorkspace 'C:\\eShopBuild'
    }

  }
  stages {
    stage('build') {
      steps {
       bat """
echo %PATH%
PATH=%PATH%;C:\\Program Files (x86)\\MSBuild\\14.0\\Bin
cp %WORKSPACE%
build.cmd
          """
        
       
      }
    }
  }
}
