pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Vikascoditas/cicd.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

    

        stage('Deploy') {
            steps {
                echo 'Deploying to production server...'
                bat 'python app.py'
            }
        }
    }
}
