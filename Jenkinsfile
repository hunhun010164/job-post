pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'sudo /root/.nvm/versions/node/v18.16.1/bin/npm install -g npm@latest'
                sh 'sudo /root/.nvm/versions/node/v18.16.1/bin/npm install styled-components@latest'
                sh 'sudo /root/.nvm/versions/node/v18.16.1/bin/npm run build'
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
