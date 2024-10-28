pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo "sh 'npm install'"
            }
        }
        stage('Test') {
            steps {
                echo "sh './jenkins/scripts/test.sh'"
            }
        }
    }
}