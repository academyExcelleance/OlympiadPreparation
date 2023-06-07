node {
    checkout scm 
}
pipeline {
    agent any
     environment {
        AWS_ACCESS_KEY_ID     = credentials('jenkins-aws-secret-key-id')
        AWS_SECRET_ACCESS_KEY = credentials('jenkins-aws-secret-access-key')
     }
    stages {
        stage('Check dependency'){
             steps {
                bat '''
                     terraform --version
                    '''
             }
        }
        stage('Initialize'){
             steps {
                bat '''
                     terraform init
                    '''
             }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                bat '''
                     terraform apply
                    '''
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
