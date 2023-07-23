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
