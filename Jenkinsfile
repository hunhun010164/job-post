pipeline {
    agent {
        docker {
            image node:18-alpine
            args '-u root:root'
        }
    }

    stages {
        stage('Build') {
            steps {
                sh 'npm install -g npm@latest'
                sh 'npm install styled-components@latest'
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                sh 'aws s3 cp /var/lib/jenkins/workspace/Jobpost/out/ s3://p3l1/ --recursive'
            }
        }
    }
}
