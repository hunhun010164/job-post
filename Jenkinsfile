pipeline {
    agent any

    stages {
        stage('Print Environment') {
            steps {
                sh 'echo $PATH'
            }
        }
        stage('Build') {
            steps {
                sh '/var/lib/jenkins/.nvm/versions/node/v18.17.0/bin/npm install -g npm@latest'
                sh '/var/lib/jenkins/.nvm/versions/node/v18.17.0/bin/npm install styled-components@latest'
                sh '/var/lib/jenkins/.nvm/versions/node/v18.17.0/bin/npm run build'
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
