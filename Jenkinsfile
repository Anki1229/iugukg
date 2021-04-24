pipeline{
    agent any
    environment{
        MY_FILE = fileExists '/tmp/myfile22.txt'
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
