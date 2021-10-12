pipeline {
    agent any
    stages {
        stage('RasaDemoTraining') {
            steps {
                bat 'rasa train'
            }
        }
        stage('Splitting NLU') {
            steps {
                bat 'rasa  data split nlu'
            }
        }
        stage('Testing Split NLU Test Data') {
            steps {
                bat 'rasa  test nlu  --nlu train_test_split/test_data.yml'
            }
        }
        stage('Test Splitted NLU Data') {
            steps {
                bat 'rasa.exe  test nlu --nlu data/nlu.yml'
            }
        }
    }
}
