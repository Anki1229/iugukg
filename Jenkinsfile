pipeline {
    agent any

    parameters {
      choice choices: ['DEV', 'QA', 'PROD'], description: 'Select the Environment', name: 'Environment'
    }

    stages {
    if (params.Environment == DEV){
    stage('Deploy to DEV') {
        steps {
                sh """
                echo "deploy to dev"
                """
            }
        }
}
}
}
