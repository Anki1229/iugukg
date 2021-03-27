pipeline {
    agent any

    parameters {
      choice choices: ['DEV', 'QA', 'PROD'], description: 'Select the Environment', name: 'Environment'
    }

    stages {
        
    stage ('Deploy to DEV') {
        
        if (params.Environment == DEV){
        steps {
                sh """
                echo "deploy to DEV"
                """
            }
        }
}
}
}
