pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'

                script {
                     dir('mydir') {
                     def files = findFiles() 
                     echo "This is a directory: ${files}"
                }       
                }
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