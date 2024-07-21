pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/tsega19/DockerJenkinsTest.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building project..."'
            }
        }
        stage('Build image') {
            steps {
                // script {
                //     def dockerImage = docker.build('my-test-image')
                // }
                sh 'echo "Building image..."'
            }
        }
        stage('Test image') {
            steps {
                script {
                    // docker.image('my-test-image').inside {
                        sh 'echo "Running tests..."'
                    
                    // }
                }
            }
        }
    }
}
