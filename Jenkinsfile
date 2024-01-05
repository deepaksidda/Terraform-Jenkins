pipeline {

    parameters {
        booleanParam(name: 'autoApprove', defaultValue: false, description: 'Automatically run apply after generating plan?')
    } 
    environment {
        AWS_ACCESS_KEY_ID     = "AKIAX6LQIW5ISRZBFULI"
        AWS_SECRET_ACCESS_KEY = "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"
    }

   agent  { label 'slave-1' }
    stages {
        stage('checkout') {
            steps {
                       git "https://github.com/deepaksidda/Terraform-Jenkins.git"
                        }
                    
                }
            }

        stage('terra-plan') {
            steps {
                sh "/home/ubuntu/jenkins/workspace/tef/ ; terraform init"
                sh "/home/ubuntu/jenkins/workspace/tef/ ; terraform plan -out tfplan"
                sh "/home/ubuntu/jenkins/workspace/tef/ ; terraform show -no-color tfplan > tfplan.txt"
            }
        }

    
}
