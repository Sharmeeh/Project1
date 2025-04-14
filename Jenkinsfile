pipeline {
    agent {
        docker {
            image 'python:3.9'
        }
    }
    environment {
        FLASK_APP = 'app.py'
    }
    stages {
        stage('Clone Repo') {
            steps {
                git url: 'https://github.com/Sharmeeh/Project1.git', branch: 'main'
            }
        }
        stage('Install Requirements') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run App') {
            steps {
                sh 'python app.py'
            }
        }
    }
}
