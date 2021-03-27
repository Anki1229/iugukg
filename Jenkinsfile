pipeline {
    
    agent any
    
    parameters {
        booleanParam(name: "RELEASE", defaultValue: false)
    }
    
    stages {

        stage("Build") {
            steps {
                sh "hello worl from build"
            }
        }
        
        stage("Publish Pre-Release") {
            when { expression { !params.RELEASE } }
            steps {
               sh "hello world if not flase"
            }
        }
        
        stage("Publish Release") {
            when { expression { params.RELEASE } }
            steps {
               sh "hello world if false"
            }
        }
    }
}
