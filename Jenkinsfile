
pipeline{
    agent any
    
     stages{
        stage('conditional if exists'){
            steps {
                exists()
            }
        }
    }
}

def exists = fileExists '/tmp/myfile22.txt'

if (exists) {
    echo 'Yes'
} else {
    echo 'No'
}