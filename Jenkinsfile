pipeline {
    agent any
    environment {
        CI = 'true'
        

    }
    stages {
        stage('Build') { 
            steps {
                sh "git config user.name 'xxx'"
                sh "git config user.email 'noreply@xyz.com'"
                sh 'git --version' 
                sh 'git tag v1.0.0'
                sh 'git push origin v1.0.0'
                sh 'git tag -n3'
                // sh 'echo $AWS_SECRET_ACCESS_KEY'
                // sh 'echo $AWS_ACCESS_KEY_ID'
            }
        }

        stage('Test') {
            steps {
                sh "echo 'Running test'"
            }
        }

    }
}