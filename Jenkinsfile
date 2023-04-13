pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'C:\Users\Coditas\AppData\Local\Programs\Python\Python310\Scripts\pip.exe\\pip install -r requirements.txt'
            }
        }
        
        stage('Deploy') {
            steps {
               bat 'python app.py'
            }
        }
    }
}
