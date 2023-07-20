pipeline {
    agent any
  
    stages {
        stage('Build') {
            steps {
                sh 'npm install -g npm'
                sh 'npm install styled-components'
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
