pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                 'pytest'
            }
        }
        stage('Deploy') {
            steps {
               'python app.py'
            }
        }
    }
}
