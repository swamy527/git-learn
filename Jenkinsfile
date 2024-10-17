pipeline {
    agent {
        node {
           label 'Agent-1'   
        }
    }
    environment {
        Greeting = 'Vachindroy...'
    }

    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'HOURS')
    }
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
         stage('second-stage') {
            steps {
                echo 'Hello babai World'
            }
        }
         stage('third-stage') {
            steps {
                echo 'Hello das World'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                     echo "Here are the environment variables"
                     sleep 10
                """
            }
        }
    }
    post {
        success {
            echo 'I succeeded!'
        }
        failure {
            echo 'I failed :('
        }
    }
}