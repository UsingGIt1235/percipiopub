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
      }
    }

    stage('batchScript') {
      steps {
        bat(script: 'cp C:\\Users\\Simone\\Documents\\zur\\percipiopub\\pom.xml C:\\Users\\Simone\\Documents\\zur\\percipiopub\\backup_pom', label: 'cpying', encoding: 'UTF-8', returnStatus: true, returnStdout: true)
      }
    }

    stage('getIP') {
      steps {
        bat(script: 'ipconfig > C:\\Users\\Simone\\getIp2.txt', label: 'getIp', returnStdout: true, returnStatus: true)
      }
    }

    stage('Read') {
      steps {
        load 'c:\\Users\\Simone\\ipc.bat'
      }
    }

  }
}