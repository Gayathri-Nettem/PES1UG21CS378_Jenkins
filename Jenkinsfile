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
                sh 'nonexistentcommand'
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