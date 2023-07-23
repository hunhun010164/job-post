pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                    # Find the absolute path of npm
                    NPM_PATH=$(which npm)
                    # Use the absolute path of npm to install npm@latest
                    $NPM_PATH install -g npm@latest
                '''
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
