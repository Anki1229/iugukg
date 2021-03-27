pipeline {
    
    agent any
    
    parameters {
        booleanParam(name: "RELEASE", defaultValue: false)
    }
    
    stages {

        stage("Build") {
            steps {
                sh '''echo "hello world"
'''
            }
        }
        
        stage("Publish Pre-Release") {
            when { expression { !params.RELEASE } }
            steps {
               sh '''echo "hello world if not false"
'''
            }
        }
        
        stage("Publish Release") {
            when { expression { params.RELEASE } }
            steps {
               sh '''echo "hello world if false"
'''
            }
        }
    }
}
