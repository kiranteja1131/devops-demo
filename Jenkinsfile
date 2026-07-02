pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                bat '"C:\\Users\\kiran\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" -m pip install -r requirements.txt'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t devops-demo .'
            }
        }
        stage('Tag Docker Image') {
            steps {
                bat 'docker tag devops-demo:latest kiran626/devops-demo:latest'
            }
        }
        stage('Push Docker Image') {
            steps {
                bat 'docker push kiran626/devops-demo:latest'
            }
        }
    }
}
    