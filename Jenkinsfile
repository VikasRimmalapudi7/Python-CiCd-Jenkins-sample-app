pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                bat 'pip install -r requirements.txt'
               
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
