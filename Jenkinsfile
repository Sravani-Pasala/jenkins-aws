pipeline {
  agent any
  stages {
    stage('Execute Terraform') {
      steps {
        echo 'creating vpc'
       
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
      
  }
 }
}
