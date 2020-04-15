pipeline {
    agent any
    environment {
        CI = 'true'
        AWS_ACCESS_KEY_ID = credentials('jenkins-aws-secret-key-id')
        AWS_SECRET_ACCESS_KEY = credentials('jenkins-aws-secret-access-key')

    }
    stages {
        stage('Build') { 
            steps {
                sh 'echo Hello' 
                sh 'npm -v'
                sh 'node -v'
                sh 'echo $AWS_SECRET_ACCESS_KEY'
                sh 'echo $AWS_ACCESS_KEY_ID'
            }
        }

        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }

    }
}