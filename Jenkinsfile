pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                terraform init
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