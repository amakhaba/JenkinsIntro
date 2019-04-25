pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo "Building..."
                sh label: '', script: 'pip install figlet'
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