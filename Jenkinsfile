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
        bat(returnStatus: true, returnStdout: true, script: 'cd rasa')
      }
    }

  }
}