pipeline {
    agent any

    stages {
        stage('Build') {
            steps{
                sh 'docker build -t example:dev .'
            }
        }
        stage('Deploy') {
            steps{
                sh 'docker run -v ${PWD}:/app -v /app/node_modules -p 4201:4200 --rm example:dev'
            }
        }
    }
}
