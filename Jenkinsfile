pipeline {
    agent {
        any
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'echo Hello' 
                sh 'npm -v'
                sh 'node -v'
            }
        }

        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }

    }
}