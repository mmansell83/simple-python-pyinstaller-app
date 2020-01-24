pipeline {
    agent none
    
    docker.withServer('tcp://$DOCKER_HOST') {
        docker.image('python:2-alpine').inside {
            stages {
                stage('Build') {
                    sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
                }
            }
        }
    }
}
