pipeline {
    agent any 
    environment {
        ENV_URL = "pipeline.google.com"
        SSH_CRED = credentials('ssh-cred') 
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    // triggers { cron('*/1 * * * *') } # Sample Change....
    triggers { pollSCM('*/1 * * * *') }
    stages {
        stage('Build') {
            steps {
                sh ''' 
                    echo "Budling the nodeJS App"
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
        stage('Maven') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}