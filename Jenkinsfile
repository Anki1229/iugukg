pipeline {
    agent any 
    stages {
        stage('Example Build') {
            agent any
            steps {
                echo 'Hello, Liquibase'
                liquibaseplan()
                }
                    
            }
        }
        stage('Example Test') {
            agent any
            steps {
                echo 'Hello, JDK'
            }
        }

def liquibaseplan(){

    container('mongodbcon'){
                    sh '''liquibase validate
                    '''
                }      
}
}