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
                      if (f.directory) {
                         echo "This is a directory: ${f.name}"
                         dirname = f.directory
                         if(f.name != '.git')
                         {
                          echo "inside loop: ${dirname}"
                          sh "cd ${workspace}/${dirname}/"
                          sh 'pwd'
                          sh 'ls'
                         }
                      }
                    }
                     sh 'python3 --version'
                }
            }
        }
    }
}