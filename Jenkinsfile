pipeline {
  agent {
    node {
      label 'IBM'
    }

  }
  stages {
    stage('RasaDemoSCM pull') {
      steps {
        echo 'Rasa Train'
        readTrusted 'https://github.com/mercurialmindsrpa/RasaDemo.git'
      }
    }

  }
}