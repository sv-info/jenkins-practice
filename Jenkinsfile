pipeline {
    agent {
        label 'Agent-1'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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