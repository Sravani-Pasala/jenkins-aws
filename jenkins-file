pipeline {
  agent any
  stages {
    stage('Execute Terraform') {
      steps {
        echo 'creating vpc'
        sh '''(cd /var/lib/jenkins/terraformPractice/; sudo git pull)
cp -f /var/lib/jenkins/variables/variables.tf variables.tf
cp -f /var/lib/jenkins/terraformPractice/aws-vpc.tf aws-vpc.tf
terraform init
terraform plan
terraform apply'''
      }
    }


  stage('Sleep 5.5 min') {
      steps {
        echo 'Sleeping'
        sleep(time: 330, unit: 'SECONDS')
        echo 'Waking up'
      }
    }

stage('Destroy') {
      steps {
        echo 'Destroying'
        sh 'terraform destroy -force || true'
      }
  }
 }
}
