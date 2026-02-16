pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/codeproject365-aim/CloudForge.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building CloudForge..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying App..."
            }
        }
    }
}

