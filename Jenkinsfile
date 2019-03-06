pipeline {
    agent none
    stages {
        stage('build') {
            agent { 
            dockerfile { 
                filename 'Dockerfile.build1'
            } 
 
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


