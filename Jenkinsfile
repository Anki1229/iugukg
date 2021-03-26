pipeline {
    agent any

    parameters {
      choice choices: ['DEV', 'QA', 'PROD'], description: 'Select the Environment', name: 'Environment'
    }

   
    if (params.Environment == DEV){
    stages {	
    stage ('Deploy to DEV') {
        steps {
                sh """
                echo "deploy to DEV"
                """
            }
        }
}
}
}
