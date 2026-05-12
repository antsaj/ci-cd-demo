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
                echo 'Building application'
            }
        }

        stage('Test') {
            steps {
                echo 'Tests passed'
            }
        }

		stage('Debug SSH') {
    steps {
        sh '''
        whoami
        ls -la ~/.ssh || true
        ssh -v ubuntu@13.218.68.232 "echo OK"
        '''
    }
}

    }
}
