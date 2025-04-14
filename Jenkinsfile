pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo "Cloning the repo..."
                // If using GitHub, use git URL
                // git url: 'https://github.com/Sharmeeh/Project1.git'
            }
        }

        stage('Install dependencies') {
            steps {
                echo "Installing dependencies..."
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Flask app') {
            steps {
                echo "Starting Flask app..."
                sh 'nohup python3 app.py &'
            }
        }
    }
}
