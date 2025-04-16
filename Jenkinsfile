pipeline {
    agent any
    
    
    stages {
        stage('Clone Repo') {
            steps {
                git url: 'https://github.com/Sharmeeh/Project1.git', branch: 'main'
            }
        }
       stage('Build Docker Image') {
            steps {
                script {
                    docker.build('jenkins-demo-image')
                }
            }
        }
        stage('Run Container') {
            steps {
                script {
                    docker.image('jenkins-demo-image').run('-d -p 5000:5000')
                }
            }
        }
    }
}
