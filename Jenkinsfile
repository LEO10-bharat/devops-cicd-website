pipeline {
    agent any

    stages {
        stage('Download Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/LEO10-bharat/devops-cicd-website.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-website:latest .'
            }
        }

        stage('Verify Docker Image') {
            steps {
                sh 'docker images devops-website'
            }
        }
    }
}
