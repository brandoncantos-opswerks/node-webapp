pipeline {
    agent {
        label 'linux'
    }
    
    stages {
        stage {
            steps {
                script {
                    checkout scm
                    def dockerImage = docker.build('my-image:latest')
                    dockerImage.push()
                }
            }
        }
    }
}
