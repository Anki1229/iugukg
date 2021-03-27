pipeline {
    
    agent any
    
    parameters {
  choice choices: ['DEV', 'QA', 'TEST'], description: 'Select the env', name: 'ENVIRONMENT'
}
    
    stages {

        stage("Build") {
            steps {
                sh '''echo "hello world"
'''
            }
        }
        
        stage("Deploy to dev") {
            when { expression { params.ENVIRONMENT == DEV } }
            steps {
               sh '''echo "hello world from DEV"
'''
            }
        }
        
        stage("deploy to qa") {
            when { expression { params.ENVIRONMENT == QA } }
            steps {
               sh '''echo "hello world from QA"
'''
            }
        }
    }
}
