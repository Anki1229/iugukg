pipeline {
    agent any
    parameters {
        string(name: 'ENVIRONMENT', defaultValue: 'Hello, I am QA', description: 'How should I greet the world?')
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.ENVIRONMENT} World!"
            }
        }
    }
}
