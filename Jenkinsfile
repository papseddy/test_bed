pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'yum install ansible'
      }
    }

    stage('Deployment') {
      steps {
        sh '/usr/local/bin/ansible-playbook test.yaml'
      }
    }

    stage('Result') {
      steps {
        echo 'Successfull'
      }
    }

  }
}