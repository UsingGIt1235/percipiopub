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
            writeFile(file: 'OceanBlue', text: 'BlueOceanSuccess', encoding: 'UTF-8')
          }
        }

      }
    }

  }
}