pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/HG-Devops/devops-cicd-project.git'
            }
        }

        stage('Terraform Init') {
            steps {
                dir('terraform') {
                    sh 'terraform init'
                }
            }
        }

        stage('Terraform Apply') {
            steps {
                dir('terraform') {
                    sh 'terraform apply -auto-approve'
                }
            }
        }
    }
}
