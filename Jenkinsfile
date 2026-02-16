pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/codeproject365-aim/CloudForge.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cloudforge-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker stop cloudforge || true
                docker rm cloudforge || true

                docker run -d \
                -p 5000:5000 \
                --name cloudforge \
                cloudforge-app
                '''
            }
        }
    }
}
