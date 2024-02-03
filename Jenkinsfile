pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'ls'
                script {
                    String files = findFiles(glob: "**/*function*")
                }
            }
        }
    }
}