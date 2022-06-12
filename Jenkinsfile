pipeline {
    agent any
    stages {
        stage('Pre-Build') {
            steps {
                sh 'echo "Starting the script"'
                cleanWs()
                sh '''
                    echo "Hello World!"
                    echo $PWD
                    ls -la
                    docker --version
                '''
            }
        }
        stage('Build') {
            steps {
                sh'''
                    echo "Build"
                    docker build -t ngnix-hello-world .
                    docker run -d -p 80:80 ngnix-hello-world
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
