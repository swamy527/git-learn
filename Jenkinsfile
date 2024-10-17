pipeline {
    agent {
        node {
           label 'Agent-1'   
        }
    }
    environment {
        Greeting = 'Vachindroy...'
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
                     env
                """
            }
        }
    }
    post {
        success {
            echo 'I succeeded!'
        }
    }
}