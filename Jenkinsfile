pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git url: 'https://github.com/tsega19/DockerJenkinsTest.git', branch: 'main'
            }
        }
        
        stage('Build image') { // New Stage to build image
            steps {
                sh 'docker build -t my-test-image .' // Replace '.' with path to Dockerfile if needed
            }
        }
       
        stage('Test image') {
            steps {
                script {
                    sh 'docker run my-test-image echo "Running tests inside Docker container"' // Replace with your test commands
                }
            }
        }
    }
}