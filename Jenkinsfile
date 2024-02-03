pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'building..'
                sh 'pwd'
                sh 'ls'
                node {
                    
                     def files = findFiles() 
                     echo "This is a directory: ${files}"
                }       
                
            }
        }

        stage('Test') {
            steps {
                echo 'testing'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
                echo 'deploy'
            }
        }

    }
}