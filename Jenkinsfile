pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'echo Building app'
            }
        }

        stage('Test') {
            steps {
                sh 'echo Tests OK'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to second EC2 via SSH'
            }
        }
    }
}
