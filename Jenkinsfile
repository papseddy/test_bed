pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Starting Build'
            sleep 3
            node(label: 'ubuntu_test') {
              echo 'asdfasdf'
            }

            cleanWs(cleanWhenAborted: true, cleanWhenFailure: true, cleanWhenNotBuilt: true, cleanWhenSuccess: true, cleanWhenUnstable: true, cleanupMatrixParent: true, deleteDirs: true, disableDeferredWipeout: true)
            timestamps() {
              sleep 2
            }

          }
        }

        stage('Build2') {
          steps {
            mail(subject: 'starting build', body: 'asdfasdf', to: 'papseddy@gmail.com')
          }
        }

      }
    }

    stage('deployment') {
      steps {
        sh 'echo "test"'
        fileExists 'test.yaml'
        milestone(ordinal: -1, label: 'asdf', unsafe: true)
      }
    }

  }
}