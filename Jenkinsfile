pipeline{
    agent any
    
    stages{
        stage('conditional if exists'){
            when { expression { MY_FILE == 'true' } }
            steps {
                exists()
                
            }
        }
        stage('conditional if not exists'){
            when { expression { MY_FILE == 'false' } }
            steps {
                exists()
            }
        }
    }
}

def exists = fileExists '/tmp/myfile22.txt'

if (exists) {
    echo 'Yes , the file exists'
} else {
    echo 'No, file does not exists'
}