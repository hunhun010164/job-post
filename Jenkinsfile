pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'which npm'
                sh 'sudo /var/lib/jenkins/.nvm/versions/node/v18.17.0/bin/npm install -g npm@latest'
                sh 'sudo /var/lib/jenkins/.nvm/versions/node/v18.17.0/bin/npm install styled-components@latest'
                sh 'sudo /var/lib/jenkins/.nvm/versions/node/v18.17.0/bin/npm run build'
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
