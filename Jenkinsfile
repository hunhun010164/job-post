pipeline {
    agent any

    stages {
        stage('Find Root NPM Path') {
            steps {
                script {
                    // 执行 sudo which npm 命令获取 root 用户下的 npm 路径
                    def rootNpmPath = sh(returnStdout: true, script: 'sudo which npm').trim()
                    // 将路径存储在环境变量 ROOT_NPM_PATH 中
                    env.ROOT_NPM_PATH = rootNpmPath
                }
            }
        }
        stage('Build') {
            steps {
                sh 'sudo ${env.ROOT_NPM_PATH} install -g npm@latest'
                sh 'sudo ${env.ROOT_NPM_PATH} install styled-components@latest'
                sh 'sudo ${env.ROOT_NPM_PATH} run build'
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
