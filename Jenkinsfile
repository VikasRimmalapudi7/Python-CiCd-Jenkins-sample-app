pipeline {
    agent any

    environment {
        APP_PID_FILE = 'flask_app.pid'
    }

    stages {
        stage('Preparation') {
            steps {
                script {
                    if (fileExists(env.APP_PID_FILE)) {
                        bat "FOR /F %i IN (flask_app.pid) DO taskkill /F /PID %i"
                        bat "del ${env.APP_PID_FILE}"
                    }
                }
            }
        }

        stage('Build') {
            steps {
                bat 'C:\\Users\\Coditas\\AppData\\Local\\Programs\\Python\\Python310\\python.exe -m pip install -r requirements.txt'
            }
        }

        stage('Deploy') {
            steps {
                bat 'C:\\Users\\Coditas\\AppData\\Local\\Programs\\Python\\Python310\\python.exe app.py > app.log 2>&1 & echo %! > ${env.APP_PID_FILE}'
            }
        }
    }

    post {
        always {
            script {
                if (fileExists(env.APP_PID_FILE)) {
                    bat "FOR /F %i IN (flask_app.pid) DO taskkill /F /PID %i"
                    bat "del ${env.APP_PID_FILE}"
                }
            }
        }
    }
}
