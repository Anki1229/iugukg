pipeline {
    agent any

    parameters {
      choice choices: ['DEV', 'QA', 'PROD'], description: 'Select the Environment', name: 'Environment'
    }

    stages {
    stage('Deploy to Production') {
        when {
            expression {
               return params.Environment == 'PROD'
            }
        }
        steps {
                sh """
                echo "deploy to production"
                """
            }
        }
}
}

