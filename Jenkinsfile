pipeline {
    agent any
parameters {
  choice choices: ['DEV', 'QA', 'TESTING'], description: 'Select the environment', name: 'ENVIRONMENT'
}

    stages {
       
        stage ('Test 3: Master') {
    when { branch 'master' }
    steps { 
        echo 'I only execute on the DEV branch.' 
    }
}

stage ('Test 3: Dev') {
    when { not { branch 'master' } }
    steps {
        echo 'I execute on non-master branches.'
    }
}
        }
    }

