pipeline {
    agent { 
        node {
            label 'docker-agent-python'
            }
      }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                ls
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
