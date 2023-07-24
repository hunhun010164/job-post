pipeline {
    agent any

    environment {
        PATH = "/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/path/to/node/bin:/path/to/npm/bin"
    }

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
