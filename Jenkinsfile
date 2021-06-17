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
        bat(script: 'cp C:\\Users\\Simone\\Documents\\zur\\pom.xml C:\\Users\\Simone\\Documents\\zur\\pom_backup', label: 'ip-address', returnStdout: true, returnStatus: true, encoding: 'UTF-8')
      }
    }

  }
}