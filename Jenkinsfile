pipeline {
    agent any
parameters {
  choice choices: ['DEV', 'QA', 'TESTING'], description: 'Select the environment', name: 'ENVIRONMENT'
}

    stages {
        stage('test') {
            steps {
                sh 'echo hello'
            }
        }
        stage('test1') {
            steps {
                sh 'echo $TEST'
            }
        }
        stage('test3') {
            steps {
                script {
                    if (env.ENVIRONMET == 'DEV') {
                        echo 'I only execute on the DEV branch'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
            }
        }
    }
}
