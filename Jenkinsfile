pipeline {
    agent any

    environment {
        NVM_DIR = "$HOME/.nvm"
    }
    stages {
        stage('Build') {
            steps {
                sh '''
                export NVM_DIR="$HOME/.nvm" // 将 NVM_DIR 设置为 Jenkins 用户的 .nvm 目录
                [ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"
                '''
                // 安装所需的 Node.js 版本
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
