pipeline {
    agent { 
        node {
            label 'docker-agent-python'
            }
      }
    stages {
        stage('Fetch') {
            steps {
                echo "Fetching."
                sh '''
                cd new
                python3 hello.py
                '''
            }
        }
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                python3 now.py
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                python3 now.py
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                python3 now.py
                '''
            }
        }
    }
}
