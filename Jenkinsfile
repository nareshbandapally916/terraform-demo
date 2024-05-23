pipeline {
    agent any
    tools {
        terraform 'terraform-1.8'
    }
    stages {
        stage('SCM Checkout') {
            steps {
                git credentialsId: 'github-cred', url: 'https://github.com/nareshbandapally916/terraform-demo'
            }
        }
        stage('Terraform Init') {
            steps {
                sh 'terraform init'    
            }
        }
        stage('Terraform Apply') {
            steps {
                sh 'terraform plan'
            }
        }
    }

}
