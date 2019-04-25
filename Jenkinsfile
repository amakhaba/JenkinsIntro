pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo "Building..."
                sh apt-get install figlet
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