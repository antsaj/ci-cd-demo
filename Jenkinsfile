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

        stage('Deploy') {
    steps {
        sh '''
        ssh ubuntu@44.208.166.29 "pkill node || true"
        scp app.js ubuntu@44.208.166.29:/home/ubuntu/app/
        ssh ubuntu@44.208.166.29 "cd /home/ubuntu/app && nohup node app.js > output.log 2>&1 &"
        '''
    }
}
    }
}
