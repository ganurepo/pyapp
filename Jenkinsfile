pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'mkdir -p builds/packages'
                sh 'cd builds'
                sh 'pip install -r requirements.txt /packages'
                sh 'ls packages'              
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
                          mkdir ${dirname}
                          
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