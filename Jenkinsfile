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
                sh '''cd /var/jenkins_home/workspace/pipeline
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
}