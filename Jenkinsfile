node {    
    docker.withServer(env.DOCKER_HOST) {
        docker.image('python:2-alpine').inside {
            stage("Build - compile python") {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
            }
        }
    }
}
