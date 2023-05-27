pipeline {
    agent none 
    stages {
        stage('Build') { 
            agent {
                docker {
                    image 'python' 
                }
            }
            steps {
                sh 'python -m py_compile app.py' 
                stash(name: 'compiled-results', includes: '/*.py*') 
            }
        }
    }
}

