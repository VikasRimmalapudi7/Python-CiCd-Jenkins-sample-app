pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        
        stage('Deploy') {
           
            steps {
               bat 'python app.py'
            }
        
        }
    }
}
