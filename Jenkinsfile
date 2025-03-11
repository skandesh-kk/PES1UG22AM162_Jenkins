pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project...'
                    sh 'g++ -o hello_exec main/hello.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the test...'
                    sh './hello_exec'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the project...'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
