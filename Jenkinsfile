pipeline {
    agent none
    stages {
        stage('build') {
            agent { 
                dockerfile { 
                    filename 'Dockerfile.build1'
                    additionalBuildArgs '--no-cache'
                } 
            }
 
            steps {
                sh 'echo "TEST"'
                sh 'ls'
                sh 'pwd'
                sh 'cp examples/tutorial_example.c .'
                dir('build'){
                    writeFile file:'dummy', text:''
                }
                sh 'cd build; cmake ..'
                sh 'cd build; VERBOSE=TRUE make'
            }
        }
    }
}


