pipeline {
    agent none
    stages {
        stage('build') {
            agent { 
                dockerfile { 
                    filename 'Dockerfile.build1'
                } 
            }
 
            steps {
                sh 'echo "TEST"'
                sh 'ls'
                sh 'pwd'
                sh 'cd build'
                sh 'cmake ..'
                sh 'VERBOSE=TRUE make'
            }
        }
    }
}


