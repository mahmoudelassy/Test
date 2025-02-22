pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/mahmoudelassy/Test.git', branch: 'master')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('error') {
          steps {
            dockerNode(image: 'python:3.9.21-alpine3.21') {
              sh 'python3 --version'
            }

          }
        }

      }
    }

  }
}