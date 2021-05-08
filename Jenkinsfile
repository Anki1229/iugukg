reponame='iugukg'
pipeline{
    agent any
    environment{
        MY_FILE = '/tmp/myfile22.txt'
    }
     stages{
        
        stage('plan dev'){
            steps{
                script{
                    withCredentials([
                        [ 
                          credentialsId: 'awsuser',
                          passwordVariable: 'AWS_ACCESS_SECRET_KEY',
                          usernameVariable: 'AWS_ACCESS_KEY_ID'
                        ]
                    ]) {
                        withEnv([
                            'ENVIRONMENT=dev'
                        ]){
                            liquibaseplan()
                    } 
                }
            }
        }              
    }
}    
def liquibaseplan(){
    agent any
    sh '''
        cd $reponame
        echo "finding txt file"
        '''
    }
}