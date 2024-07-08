pipeline {
    
    stages {
        stage('Clone repository') {
            steps {
                git url: 'https://github.com/tsega19/DockerJenkinsTest.git', branch: 'main'
            }
        }
       
        stage('Test image') {
            steps {
                script {
                    myImage.inside {
                        sh 'echo "Running tests inside Docker container"'
                        // Add your test commands here
                    }
                }
            }
        }
    }
}
