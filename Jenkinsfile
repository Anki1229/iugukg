pipeline {
    agent none 
    stages {
        stage('Example Build') {
            agent any
            steps {
                echo 'Hello, Liquibase'
                    sh '''liquibase validate
                    '''
            }
        }
        stage('Example Test') {
            agent any
            steps {
                echo 'Hello, JDK'
            }
        }
    }
}