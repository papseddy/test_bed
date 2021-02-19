pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'sudo yum install ansible'
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

  }
}