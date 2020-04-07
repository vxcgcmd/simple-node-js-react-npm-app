pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-u root:root -p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh '/usr/bin/sudo npm install' 
            }
        }
    }
}