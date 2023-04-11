pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build and Test') {
            steps {
                bat 'pip install -r requirements.txt'
                bat 'python tests.py'
            }
        }

        stage('Deploy') {
            when {
                branch 'master'
            }
            steps {
                bat 'python app.py'
            }
        }
    }
}
