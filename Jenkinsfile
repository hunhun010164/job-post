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
                sh 'usr/binnpm install -g npm@latest'
                sh 'usr/binnpm install styled-components@latest'
                sh 'usr/binnpm run build'
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
