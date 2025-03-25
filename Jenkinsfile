pipeline {
    agent any 
    environment {
        ENV_URL = "pipeline.google.com"
    }
    stages {
        stage('Build') {
            steps {
                echo "Budling the nodeJS App"
                echo "Env Url is ${ENV_URL}"
            }
        }
        stage('Deploying') {
            steps {
                echo "Deploying the nodeJS App"
                echo "Env Url is ${ENV_URL}"
            }
        }
        stage('Checks') {
            steps {
                echo "Running Post Deployment Checks"
            }
        }
    }
}