pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'C:\\Users\\Coditas\\AppData\\Local\\Programs\\Python\\Python310\\Scripts\\pip.exe install -r requirements.txt'
            }
        }
        
        stage('Deploy') {
            steps {
               bat 'C:\\Users\\Coditas\\AppData\\Local\\Programs\\Python\\Python310\\python.exe\\python app.py'
            }
        }
    }
}
