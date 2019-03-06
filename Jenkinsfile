pipeline {
    agent { 
        dockerfile { 
            filename 'Dockerfile.build1'
        } 
    }
    stages {
        stage('build') {
            steps {
                sh 'echo "TEST"'
                sh 'python3 --version'
                sh 'ls'
                sh 'mkdir build'
                sh 'cd build'
                sh 'cmake ..'
                sh 'VERBOSE=TRUE make'
            }
        }
    }
}


