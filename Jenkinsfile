pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'sudo yum install ansible -y'
      }
    }

    stage('Deployment') {
      steps {
        sh 'sudo /usr/local/bin/ansible-playbook test.yaml'
      }
    }

    stage('Result') {
      steps {
        echo 'Successfull'
      }
    }
    stage("Calling is all successfull"){
        steps{
            echo "====++++executing Calling is all successfull++++===="
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
  }
}