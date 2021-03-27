pipeline {
    agent any
parameters {
  choice choices: ['DEV', 'QA', 'TESTING'], description: 'Select the environment', name: 'ENVIRONMENT'
}

    stages {
       
        stage('Deploy to Dev') {
            steps {
                script {
                    if (env.ENVIRONMET == 'DEV') {
                        echo 'I only execute on the DEV branch'
                    } 
                    if (env.ENVIRONMET == 'QA') {
                        echo 'I only execute on the QA branch'
                    } 
                }
            }
        }
    }
}
