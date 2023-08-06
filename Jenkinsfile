pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'sudo /var/lib/jenkins/.nvm/versions/node/v18.17.0/bin/npm install -g npm@latest'
                sh 'sudo /var/lib/jenkins/.nvm/versions/node/v18.17.0/bin/npm install styled-components@latest'
                sh 'sudo /var/lib/jenkins/.nvm/versions/node/v18.17.0/bin/npm run build'
            }
        }
        stage('Deploy') {
            steps {
                sh 'aws s3 cp /var/lib/jenkins/workspace/Jobpost/out/ s3://p3l1/ --recursive'
            }
        }
    }
}
