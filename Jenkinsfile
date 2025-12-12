pipeline {
    agent {
        label 'Agent-1'
    }
    environment{
        course="jenkins"
    }
     options {
        timeout(time: 1, unit: 'MINUTES') 
        disableConcurrentBuilds()
    }
    parameters {
        // Environment selection
        choice(
            name: 'ENV',
            choices: ['dev', 'qa', 'prod'],
            description: 'Select the environment to deploy to'
        )
    }
    stages {
        stage('Build') {
            steps {
                script{
                sh """
                echo "Hello Build"
                Select the environment to deploy to ${params.ENV}
                env
                """
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success { 
            echo 'Hello Success!'
        }
        failure { 
            echo 'Hello, Failure!'
        }
        changed { 
            echo 'Hello!.. Changed!'
        }
    }
}