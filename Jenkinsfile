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
                     filesByGlob = findFiles(glob: "**");
                }

            }
        }
    }
}