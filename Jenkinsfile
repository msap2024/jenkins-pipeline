pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // checkout([$class:'GitSCM',branches:[[name:'*main']],extensions:[],userREmoteConfigs:[[url:'https://github.com/msap2024/jenkins-pipeline.git']]])
            }
        }
        
        stage("terraform init") {
            steps {
                sh ('terraform init')
            }
        }
        stage("terraform plan") {
            steps {
                echo "Terraform plan"
                sh ('terraform plan')
            }
        }
    }
}