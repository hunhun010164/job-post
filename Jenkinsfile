pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'sudo npm install -g npm@latest'
                sh 'sudo npm install styled-components@latest'
                sh 'sudo npm run build'
            }
        }
        stage('Deploy') {
            steps {
                sh 'aws s3 cp /var/lib/jenkins/workspace/Jobpost/out/ s3://p3l1/ --recursive'
            }
        }
    }
}
