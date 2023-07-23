pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    def npmPath = sh(returnStdout: true, script: 'which npm').trim()
                    sh "sudo ${npmPath} install -g npm@latest"
                    sh 'sudo ${npmPath} install -g npm@latest'
                    sh 'sudo ${npmPath} install styled-components@latest'
                    sh 'sudo ${npmPath} run build'
                }
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
