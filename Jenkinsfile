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

     /*   stage('Plan') {
            steps {
                sh '/home/ubuntu/jenkins/workspace/tef/ ; terraform init'
                sh "/home/ubuntu/jenkins/workspace/tef/ ; terraform plan -out tfplan"
                sh '/home/ubuntu/jenkins/workspace/tef/ ; terraform show -no-color tfplan > tfplan.txt'
            }
        }
        stage('Approval') {
           when {
               not {
                   equals expected: true, actual: params.autoApprove
               }
           }

           steps {
               script {
                    def plan = readFile 'terraform/tfplan.txt'
                    input message: "Do you want to apply the plan?",
                    parameters: [text(name: 'Plan', description: 'Please review the plan', defaultValue: plan)]
               }
           }
       }

        stage('Apply') {
            steps {
                sh "pwd;cd terraform/ ; terraform apply -input=false tfplan"
            }
        }
    }
*/
  }
