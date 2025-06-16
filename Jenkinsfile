pipeline {
    agent any
    options {
        timestamps() // Adds timestamps to the console output
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code from SCM...'
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Starting the build process...'
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                echo 'Running unit tests...'
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Simulating deployment step...'
                // Replace with real deployment command if needed
            }
        }
        stage('Notify') {
            steps {
                echo 'Pipeline completed successfully.'
            }
        }
    }
    post {
        always {
            echo 'Pipeline execution finished.'
        }
        success {
            echo 'SUCCESS: All stages executed without error.'
        }
        failure {
            echo 'FAILURE: One or more stages failed.'
        }
    }
}
