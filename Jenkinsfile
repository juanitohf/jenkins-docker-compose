pipeline {
    agent any
    stages {
        stage('verify tooling') {
            steps {
                script {
                    echo 'Building the project...'
                    sh '''
                    docker info
                    docker version
                    docker compose version
                    curl --version
                    jq --version
                    '''
                }
            }
        }
     
    }
    environment {
        DOCKER_IMAGE = 'my-docker-image:latest'
    }
}