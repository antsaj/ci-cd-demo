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
        ssh ubutnu@13.218.68.232 "pkill node || true"
        scp app.js ubutnu@13.218.68.232:/home/ubuntu/app/
        ssh ubutnu@13.218.68.232 "cd /home/ubuntu/app && nohup node app.js > output.log 2>&1 &"
        '''
    }
}
    }
}
