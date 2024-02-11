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
                     
                     
                     files = findFiles();
                     files.each { f -> 
                      if (f.directory && f.) {
                         echo "This is a directory: ${f.name}"
                         if(f.name != '.git')
                         {
                          echo "inside loop: ${f.name}"
                          sh "cd ${f.name}"
                          sh 'ls'
                         }
                      }
                    }
                     //echo "${files}"
                     sh 'ls'
                     sh 'python3 --version'
                }
            }
        }
    }
}