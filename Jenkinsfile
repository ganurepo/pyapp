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

        stage('Test') {
            steps {
                echo 'testing'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
                echo 'deploy'
            }
        }

    }
    }
}