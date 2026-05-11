pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/antsaj/ci-cd-demo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'nohup node app.js > output.log 2>&1 &'
            }
        }
    }
}
