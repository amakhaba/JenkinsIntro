pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo "Building..."
                sh label: '', script: 'apt install figlet'
                sh label: '', script: 'figlet Building...'
            }
        }
        stage("Test") {
            steps {
                echo "Testing..."
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploying..."
            }
        }    
    }
}