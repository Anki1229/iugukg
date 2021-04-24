pipeline{
    agent any
    environment{
        MY_FILE = fileExists '/iugukg/serverless.yml'
    }
    stages{
        stage('conditional if exists'){
            when { expression { MY_FILE == 'true' } }
            steps {
                
                
            }
        }
        stage('conditional if not exists'){
            when { expression { MY_FILE == 'false' } }
            steps {
                
            }
        }
    }
}
