pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'ls'
                echo '${env.WORKSPACE}'
                script {
                     filesByGlob = findFiles(glob: "*function*");
                }

            }
        }
    }
}