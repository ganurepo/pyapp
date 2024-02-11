pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'               
                script {
                     def path = "${workspace}\builds"
                     fileOperations([folderCreateOperation(folderPath: path)])
                     cd path
                     pwd
                     filesByGlob = findFiles(glob: "*function*");
                     echo "${filesByGlob}"
                     sh 'ls'
                     sh 'python3 --version'
                }
            }
        }
    }
}