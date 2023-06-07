node {
    checkout scm 
}
pipeline {
    agent any

    stages {
        stage('Check dependency'){
             steps {
                bat '''
                     terraform --version
                    '''
             }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
