pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS378-1'
                script {
                    sh 'g++ main.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './output'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
                // Add deployment steps if needed
            }
        }
    }
    post {
        failure {
            script {
                error 'Pipeline failed'
            }
        }
    }
}