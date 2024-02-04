pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'ls'
                echo 'change in pipeline'

               
                script {
                     def path = "${workspace}\builds"
                     fileOperations([folderCreateOperation(folderPath: path)])
                     filesByGlob = findFiles(glob: "*function*");
                     echo "${filesByGlob}"
                     sh 'ls'
                }
            }
        }
    }
}