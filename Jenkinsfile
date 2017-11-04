pipeline {
    agent {
        docker {
            image 'node:latest'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
                archiveArtifacts artifacts: 'build/**/*', fingerprint: true
            }
        }
    }
}
