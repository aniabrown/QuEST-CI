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
                dir('build'){
                    writeFile file:'dummy', text:''
                }
                sh 'cd build; cmake ..'
                sh 'VERBOSE=TRUE make'
            }
        }
    }
}


