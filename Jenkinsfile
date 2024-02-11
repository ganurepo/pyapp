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
                         
                         if(f.name != '.git')
                         {
                          dirname = f.name
                          echo "inside loop: ${dirname}"
                          sh "cd ${workspace}/${dirname}/"
                          sh """ 
                          #!/bin/bash
                          cd ${dirname}
                          ls -l
                          """ 
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