pipeline {
  agent any
  stages {
    stage('welcome') {
      parallel {
        stage('welcome') {
          steps {
            echo 'hello from blueocean'
          }
        }

        stage('WriteFileToWorkspace') {
          steps {
            writeFile(file: 'c:/OceanBlue.txt', text: 'BlueOceanSuccess', encoding: 'UTF-8')
          }
        }

      }
    }

    stage('Staging') {
      steps {
        echo 'deploy'
        bat(script: 'bat \'ipconfig\'', encoding: 'utf-8', label: 'ip-address', returnStdout: true, returnStatus: true)
        powershell(script: 'C:\\Users\\Simone\\ipc.ps1', returnStdout: true, returnStatus: true)
      }
    }

  }
}