pipeline {
    agent { label 'AGENT-1'}
    environment { 
        PROJECT = 'EXPENSE'
        COMPONENT = 'BACKEND' 
    }

     options {
        disableConcurrentBuilds()
        timeout(time: 5, unit: 'SECOND')
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                       echo "Hello , this is build"
                       echo "project:$PROJECT"
                       sleep 15
                       """
                }
               
            }
        }

        stage('Test') {
            steps {
                script {
                    sh """
                       echo "Hello , this is Test"
                       """
                }
                
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh """
                       echo "Hello , this is Deploy"
                       """
                }
                
            }
        }
    }

    post { 
    
        always { 
            echo 'I will always say hello again!'
        }
        failure { 
            echo 'This session runs when pipeline failure'
        }
        success { 
            echo 'This session runs when pipeline success'
        }
    }
}