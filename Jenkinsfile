pipeline {
   agent any
	
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                 echo "install"
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
                git merge master

            }
        }
        stage('Deploy for production') {
            when {
                branch 'production'
            }
            steps {
                git merge master

            }
        }
    }
}
