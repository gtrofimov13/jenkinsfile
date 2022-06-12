pipeline {
    agent any
    stages {
        stage('Pre-Build') {
            steps {
                sh 'echo "Starting the script"'
                cleanWs()
                sh '''
                    echo "Hello World!"
                    docker --version
                '''
            }
        }
        stage('Build') {
            steps {
                sh'''
                    echo "Build"
                    docker run --rm hello-world
                '''
            }
        }
        stage('Test'){
            steps {
                sh '''
                    echo "Test"
                '''
            }
        }
        stage('Deploy') {
            steps {
               sh'''
                  echo "Deploying"
                '''
            }
        }
    }
}
