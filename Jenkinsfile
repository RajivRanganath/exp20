pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t sample-webapp .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 8087:8080 sample-webapp'
            }
        }
    }
}