pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/shahid/node-js.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t demo-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d demo-app'
            }
        }
    }
}
