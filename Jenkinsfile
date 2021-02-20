pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'sudo yum install ansible -y'
      }
    }

    stage("unit_test"){
        steps{
            sh 'ansible-playbook test.yaml --check --diff'
      }
    }
    stage('Deployment') {
      steps {
        sh 'sudo /usr/local/bin/ansible-playbook test.yaml'
      }
    }
  }
  post{
            always{
                echo "====++++always++++===="
            }
            success{
                echo "====++++Calling is all successfull executed successfully++++===="
            }
            failure{
                echo "====++++Calling is all successfull execution failed++++===="
            }
    
        }
}