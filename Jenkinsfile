pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo "Building..."
                sh label: '', script: 'apt install figlet'
                sh figlet "Building"
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