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
        stage('Deliver for developmentNew') {
            when {
                branch 'development'
            }
            steps {
                merge master
				checkout master
				merge development

            }
        }
        stage('Deploy for production') {
            when {
                branch 'production'
            }
            steps {
                merge master

            }
        }
    }
}
