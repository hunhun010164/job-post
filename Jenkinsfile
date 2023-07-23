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
                def npmPath = sh(returnStdout: true, script: 'which npm').trim()
                sh '${npmPath} install -g npm@latest'
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
