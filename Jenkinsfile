 pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Assuming 'PES2UG21CS586-1' is a parameter, otherwise replace it with your appropriate build command
                    build 'PES2UG21CS586-1'
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
                script {
                    echo 'deploy'
                    // Add your deployment steps here
                }
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

