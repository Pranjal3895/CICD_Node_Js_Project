pipeline {
    agent any

    stages {
        stage('Install dependencies') {
            steps {
                sh 'npm install --ignore-scripts --no-audit --no-fund --package-lock=false'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }
}
