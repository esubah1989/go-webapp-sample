pipeline {
    agent any
    tools {
        go '1.20.2'
    }
    environment {
        GO114MODULE = 'on'
        CGO_ENABLED = 0 
        GOPATH = "${JENKINS_HOME}/jobs/${JOB_NAME}/builds/${BUILD_ID}"
    }
    stages {        
        stage('Pre Test') {
            steps {
                echo 'Installing dependencies'
                sh 'go version'
        
            }
        }
        
        stage('Build') {
            steps {
                echo 'Compiling and building'
                sh 'go test test-agent/'
            }
        }
}
 }
