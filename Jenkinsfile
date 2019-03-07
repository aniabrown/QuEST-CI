pipeline {
    agent { 
        dockerfile { 
            filename 'Dockerfile.build1'
            args '-u root --rm'
        } 
    }
    stages {
        stage('build') {
 
            steps {
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
        stage('test') {
            steps {
                sh 'ls'
                sh 'pwd'
                sh 'cd build; make tests'
            }
        }

    }
}


