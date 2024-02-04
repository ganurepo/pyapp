pipeline {
    agent {
        docker { image 'python:3' }
    }

    stages {
         stage('Py') {
            steps {
                sh 'pip --version'
            }
         }

        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'ls'
                echo 'change in pipeline'
                sh 'mkdir build'
                sh 'cd build'
                sh 'pip install -r requirements.txt target=build'
                sh 'ls build'
                script {
                     filesByGlob = findFiles(glob: "*function*");
                     echo "${filesByGlob}"
                }
            }
        }
    }
}