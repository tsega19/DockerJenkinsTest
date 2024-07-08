pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git url: 'https://github.com/tsega19/DockerJenkinsTest.git', branch: 'main'
            }
        }
       
        stage('Test image') {
            steps {
                script {
                    // def myImage = docker.image('my-image:latest')
                    myImage.inside {
                        sh 'echo "Running tests inside Docker container"'
                        // Add your test commands here
                    }
                }
            }
        }
    }
}
