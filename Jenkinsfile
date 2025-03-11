pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project...'
                    sh 'g++ -o hello_exec hello_pipeline.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the test...'
                    sh 'chmod +x hello_exec'   // Ensures execution permission
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
