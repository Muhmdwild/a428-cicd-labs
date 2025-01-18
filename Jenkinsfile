/*
pipeline {
    agent {
        docker {
            image 'node:16-buster-slim' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install'
            }
        }
          stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
*/

Node {
    docker.image('node:16-buster-slim').inside('-p 3000:3000')
    stage('build'){
        sh 'npm install'

    }
    stage('test'){
        sh './jenkins/scripts/test.sh'
    }
}