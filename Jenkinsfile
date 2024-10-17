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
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['dev', 'qa', 'prod'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage('Example') {
            steps {
                echo "environment is ${params.CHOICE}"
                echo "Password: ${params.PASSWORD}"
            }
        }
        stage('variables-pull') {
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