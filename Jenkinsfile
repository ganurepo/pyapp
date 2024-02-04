pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'ls'
                echo 'change in pipeline'
                
                def path = "${workspace}\builds"
                fileOperations([folderCreateOperation(folderPath: path)])
                sh 'ls'
                script {
                     filesByGlob = findFiles(glob: "*function*");
                     echo "${filesByGlob}"
                }
            }
        }
    }
}