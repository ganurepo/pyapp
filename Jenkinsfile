pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'ls'
                node {
                    def files = findFiles() 
                }
            }
        }
    }
}