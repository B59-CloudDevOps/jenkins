pipeline {
    agent any 
    environment {
        ENV_URL = "pipeline.google.com"
        SSH_CRED = credentials('ssh-cred') 
    }
    stages {
        stage('Build') {
            steps {
                sh ''' 
                    echo Budling the nodeJS App"
                    echo "Env Url is ${ENV_URL}"
                    echo "Running env command"
                    env 
                ''' 
            }
        }
        stage('Deploying') {
            environment {
                ENV_URL = "stage.google.com"
            }
            steps {
                echo "Deploying the nodeJS App"
                echo "Stage Env Url is ${ENV_URL}"
            }
        }
        stage('Checks') {
            steps {
                echo "Running Post Deployment Checks"
            }
        }
    }
}