pipeline {
    
    agent any
    
    parameters {
        booleanParam(name: "RELEASE", defaultValue: false)
        choice(name: "DEPLOY_TO", choices: ["", "INT", "PRE", "PROD"])
    }
    
    stages {

        stage("Build") {
            steps {
                sh "./gradlew build"
            }
        }
        
        stage("Publish") {
            parallel {
                stage('Pre-Release') {
                    when { expression { !params.RELEASE } }
                    steps {
                        sh "./gradlew preRelease"
                    }
                }
                stage("Release") {
                    when { expression { params.RELEASE } }
                    steps {
                        sh "./gradlew release"
                    }
                }
            }
        }

        stage("Deploy") {
            steps {
                script {
                    switch(params.DEPLOY_TO) {
                        case "INT": echo "./deploy.sh int"; break
                        case "PRE": echo "./deploy.sh pre"; break
                        case "PROD": echo "./deploy.sh prod"; break
                    }
                }
            }
        }
    }
}
