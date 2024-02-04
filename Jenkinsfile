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
                    dir('${env.WORKSPACE}') {
                        def files = findFiles() 
            
                        files.each { f -> 
                            if (f.directory) {
                                echo "This is a directory: ${f.name}"
                            }
                        }

                    }
                }

            }
        }
    }
}