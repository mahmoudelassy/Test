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

        stage('py') {
          steps {
            dockerNode(image: 'mahmoudelassy/jap') {
              sh 'python3 --version'
            }

          }
        }

      }
    }

  }
}