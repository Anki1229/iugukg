pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo  "Running ${env.BUILD_ID} on ${env.JENKINS_URL}
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
