pipeline {
    agent any
    stages {
        stage('Pre-Build') {
            steps {
                sh 'echo "Starting the script"'
                cleanWs()
                sh '''
                    echo "Hello World!"
                '''
            }
        }
        stage('Build') {
            steps {
                sh'''
                    echo "Build"
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
