pipeline {
    agent any
    stages {
        stage('Splitting NLU Data to Training and Test Data') {
            steps {
                bat 'rasa data split nlu'
            }
        }
        stage('NLU Training on Train Data') {
            steps {
                bat 'rasa train nlu --nlu train_test_split/training_data.yml'
            }
        }
        stage('Testing NLU on Test Data and Creating New Model') {
            steps {
                bat 'rasa test nlu -m models --nlu train_test_split/test_data.yml'
            }
        }
        stage('Stories Testing') {
            steps {
                bat 'rasa test --stories data/stories.yml'
            }
        }
    }
}
