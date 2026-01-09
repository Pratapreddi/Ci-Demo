pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git 'https://github.com/Pratapreddi/Ci-Demo.git'
            }
        }

        stage('Test') {
            steps {
                sh 'python app.py'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ci-demo-image .'
            }
        }
    }
}
