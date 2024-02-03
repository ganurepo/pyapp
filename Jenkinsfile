pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'ls'
                script {
                    def rpmFiles = findFiles(glob: "**/*function*")
                }
            }
        }
    }
}