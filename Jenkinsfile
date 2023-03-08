pipeline {
    agent any
    tools {
        terraform 'Terraform'
        git 'Default'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout([$class:'GitSCM',branches:[[name:'master']],extensions:[],userRemoteConfigs:[[url:'https://github.com/msap2024/jenkins-pipeline.git']]])
            }
        }
        
        stage("Terraform init") {
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