pipeline{
    agent any
    environment{
        MY_FILE = fileExists '/iugukg/serverless.yml'
    }
    stages{
        stage('conditional if exists'){
            when { expression { MY_FILE == 'true' } }
            steps {
                echo "File exists"
                sh '''sls print
                '''
                
            }
        }
        stage('conditional if not exists'){
            when { expression { MY_FILE == 'false' } }
            steps {
                echo "File doesn't exists"
                sh '''sls deploy
                '''
            }
        }
    }
}
