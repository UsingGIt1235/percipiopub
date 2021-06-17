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
        bat(script: 'cp C:\\Users\\Simone\\Documents\\zur\\pom.xml C:\\Users\\Simone\\Documents\\zur\\percipiopub\\percipiopub\\backup_pom', label: 'cpying', encoding: 'UTF-8', returnStatus: true, returnStdout: true)
      }
    }

  }
}