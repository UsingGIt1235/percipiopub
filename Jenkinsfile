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

        stage('') {
          steps {
            writeFile(file: 'blueOcean', text: 'BlueOceanSuccess', encoding: 'UTF-8')
          }
        }

      }
    }

  }
}