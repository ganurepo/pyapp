pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'ls'
                echo 'change in pipeline'
                sh 'mkdir build'
                sh 'cd build'
                sh 'python3 --version'
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