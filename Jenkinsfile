pipeline {
    agent any

    environment {
        NVM_DIR = "$HOME/.nvm"
    }
    stages {
        stage('Build') {
            steps {
                sh 'chmod 777 -R ./job-post'
                sh 'cd job-post'
                sh 'npm install -g npm@latest'
                sh 'npm install styled-components@latest'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
