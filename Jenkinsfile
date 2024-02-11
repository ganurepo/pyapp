pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'mkdir -p builds/packages'
                sh 'pip install -r requirements.txt -t builds/packages'              
                script {
                     def path = "${workspace}\builds"
                     files = findFiles();
                     files.each { f -> 
                      if (f.directory) {
                         
                         if(f.name != '.git')
                         {
                          dirname = f.name
                          echo "inside loop: ${dirname}"
                          sh """ 
                          #!/bin/bash
                          pwd
                          cd builds
                          mkdir ${dirname}
                          pwd
                          cd ${workspace}
                          pwd
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