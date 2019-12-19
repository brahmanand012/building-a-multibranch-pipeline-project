pipeline {
    agent {
       image 'maven:3.3.3'
    }
	
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo "test"
            }
        }
        stage('Deliver for development') {
            when {
                branch 'development'
            }
            steps {
                git pull . master

            }
        }
        stage('Deploy for production') {
            when {
                branch 'production'
            }
            steps {
                git pull . master

            }
        }
    }
}
