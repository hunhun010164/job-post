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
                sh 'usr/bin/npm install -g npm@latest'
                sh 'usr/bin/npm install styled-components@latest'
                sh 'usr/bin/npm run build'
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
