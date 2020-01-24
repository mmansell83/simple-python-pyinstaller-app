pipeline {
    agent none 
    stages {
        stage('Build') { 
            docker.withServer('tcp://$DOCKER_HOST') {
                docker.image('python:2-alpine').inside {
                    steps {
                            sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
                        }
                }
            }
        }

    }
}

 
