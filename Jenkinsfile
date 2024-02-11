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
                     echo '${path}'
                     pwd
                     sh 'cd ${path}'
                     
                     files = findFiles();
                     files.each { f -> 
                      if (f.directory) {
                         echo "This is a directory: ${f.name}"
                      }
                    }
                     echo "${files}"
                     sh 'ls'
                     sh 'python3 --version'
                }
            }
        }
    }
}