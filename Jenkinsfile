
pipeline{
    agent any
    /* environment{
        MY_FILE = fileExists '/tmp/myfile22.txt'
        WORKSPACE= "/var/jenkins_home/workspace/pipeline"
    } */
 /*    stages{
        stage('conditional if exists'){
            when { expression { MY_FILE == 'true' } }
            steps {
                echo "file exists"
                sh '''cd ${WORKSPACE}
                    script.sh
                '''
            }
        }
        stage('conditional if not exists'){
            when { expression { MY_FILE == 'false' } }
            steps {
                echo "file does not exist"
            }
        }
    }
} */

def exists = fileExists '/tmp/myfile22.txt'

if (exists) {
    echo 'Yes'
} else {
    echo 'No'
}