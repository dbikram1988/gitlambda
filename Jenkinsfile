pipeline {
    agent any
    environment {
        REPO_URL = 'https://github.com/dbikram1988/gitlambda'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Pull code and build'
                git credentialsId: 'dbikram1988', url: "${REPO_URL}"
                bat 'npm install'
                bat 'npm run build'
            }
        }
        
        stage('Vulnerability assesment'){
            input {
                message "Confirm no new vulnerabilities have been discovered."
                ok "Confirm"
            }
            steps{
                echo 'Vulnerability check passed'
            }
        }
        stage('Test') {
            steps {
                echo 'Run tests and publish results'
                bat 'npm run test'
            }
        }
    }    
}
