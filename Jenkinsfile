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
    stage('pushtoecr'){
      steps {
        bat """docker tag eshop/modernizedmvc:latest 334818472548.dkr.ecr.ap-southeast-2.amazonaws.com/modernizedmvc:latest"""
        powershell """Invoke-Expression -Command (Get-ECRLoginCommand -Region ap-southeast-2).Command
        docker push 334818472548.dkr.ecr.ap-southeast-2.amazonaws.com/modernizedmvc:latest"""
       
      }
    }
  }
}
