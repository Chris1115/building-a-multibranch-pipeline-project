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
        stage('Deliver for development') {
            when {
                branch 'development' 
            }
            steps {
                echo "Doing development Process"
            }
        }
        stage('Deploy for production') {
            when {
                branch 'production'  
            }
            steps {
                echo "Doing Production Process"
            }
        }
    }
}
