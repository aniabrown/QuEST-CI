pipeline {
    agent { 
        docker { 
            image 'python:3.5.1' 
            args '-u root'
        } 
    }
    stages {
        stage('build') {
            steps {
                sh 'echo "TEST"'
                sh 'python --version'
                sh 'ls'
                sh 'cd build'
                sh 'cmake ..'
            }
        }
    }
}


