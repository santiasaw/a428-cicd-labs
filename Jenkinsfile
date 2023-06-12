pipeline {
    agent {
        docker {
            image 'node:16-buster-slim' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('cloneRepo') { 
            steps {
                git branch: 'react-app', url: 'https://github.com/santiasaw/a428-cicd-labs'
            }
        }
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}