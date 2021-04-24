pipeline{
    agent any
    environment{
        MY_FILE = fileExists '/tmp/myfile22.txt'
    }
    stages{
        stage('conditional if exists'){
            when { expression { MY_FILE == 'true' } }
            steps {
                echo "file exists"
                sh '''sls print
                '''
                
            }
        }
        stage('conditional if not exists'){
            when { expression { MY_FILE == 'false' } }
            steps {
                echo "file does not exist"
                sh '''sls deploy
                '''
            }
        }
    }
}