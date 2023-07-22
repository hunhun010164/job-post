pipeline {
    agent any
  
    stages {
        stage('Build') {
            steps {
                sh 'curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash'
                sh 'source ~/.nvm/nvm.sh'
                sh 'nvm install 14'
                sh 'nvm use 14'
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
