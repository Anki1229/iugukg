
pipeline{
    agent any
    environment{
        MY_FILE = '/tmp/myfile22.txt'
    }
     stages{
        stage('conditional if exists'){
            steps {

                sh 'cd /tmp'
                exists()
            }
        }
    }
}

def exists(){

if (fileExists('$MY_FILE')) {
    echo 'Yes'
} else {
    echo 'No'
}
}