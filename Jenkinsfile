pipeline {
    agent any

    environment {
        NVM_DIR = "$HOME/.nvm"
    }
    stages {
        stage('Build') {
            steps {
                sh 'nvm install 14' // 这里安装的是 Node.js 14，你也可以选择其他版本
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
