pipeline {
    agent any

    options {
        disableConcurrentBuilds()
        disableResume()
        timeout(time: 1, unit: 'HOURS')
    }

    stages {
        stage('Build Back End Image') {
            steps {
                sh '''
                docker build -t practical-devops:latest -f src/backend/Dockerfile .
                '''
            }
        }
    }
}