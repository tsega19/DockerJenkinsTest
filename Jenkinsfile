pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/tsega19/DockerJenkinsTest.git'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Build image') {
            steps {
                script {
                    // Ensure Docker is configured correctly
                    def dockerImage = docker.build('my-test-image')
                }
            }
        }
        stage('Test image') {
            steps {
                script {
                    docker.image('my-test-image').inside {
                        sh 'npm test'
                    }
                }
            }
        }
    }
}
