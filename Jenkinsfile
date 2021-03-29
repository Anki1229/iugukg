pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo  "Running ${env.BUILD_ID} on ${env.BUILD_NUMBER}
            }
        }
        stage('Test') {
            steps {
                echo 'Testing code..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying code....'
            }
        }
    }
}
