pipeline {
  agent any
  stages {
    stage('code') {
      steps {
        echo 'to prepare the code'
      }
    }

    stage('build') {
      steps {
        echo 'to build the code'
      }
    }

    stage('test') {
      steps {
        echo 'to test the code'
      }
    }

    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            echo 'to deploy the code'
          }
        }

        stage('test') {
          steps {
            echo 'to test the code'
          }
        }

        stage('Operate') {
          steps {
            echo 'to operate the app'
          }
        }

      }
    }

  }
}