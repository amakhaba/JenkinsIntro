pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo "Building..."
                sh label: '', script: 'make'
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint:true 
            }
        }
        stage("Test") {
            steps {
                echo "Testing..."
                /* `make check` returns non-zero on test faiures,
                * using `true` to allow the Pipeline to continue nonetheless
                */
                sh label: '', script: 'make check || true'
                junit '**/target/*.xml'
            }
        }
        stage("Deploy") {
            when {
                expression {
                    currentBuild.result == null || currentBuild.result == 'SUCCESS'
                }
            }
            steps {
                echo "Deploying..."
                sh 'make publish'
            }
        }
    }    
}