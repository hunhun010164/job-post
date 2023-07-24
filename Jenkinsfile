pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'sudo npm install -g npm@latest'
                sh 'sudo npm install styled-components@latest'
                sh 'sudo npm run build'
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
