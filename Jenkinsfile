pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo "Budling the nodeJS App"
            }
        }
        stage('Deploying') {
            steps {
                echo "Deploying the nodeJS App"
            }
        }
        stage('Checks') {
            steps {
                echo "Running Post Deployment Checks"
            }
        }
    }
}