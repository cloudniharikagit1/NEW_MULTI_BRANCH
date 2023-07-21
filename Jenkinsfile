pipeline {
    agent any 
    environment {
        DEPLOY_TO = "SIVA"

    }
    stages {
        stage ("deploy") {
            when {
              anyOf {
                BRANCH_NAME ==~ /(production|stagging)/
                environment name: 'DEPLOY_TO', value: 'SIVA'
              }
            }

            steps {
                echo " all satisfied "
            }
        }
        stage ('second stage') 
        {
            failFast true{
                parallel {
                    stage ('sonar') {
                        steps{
                            echo "performing sonar scans"
                            sleep 10
                        }
                    
                    }
                    stage ('fortify') {
                        steps {
                            echo "**** performing fortify****"
                            sleep 10
                        }
                    }
                }
            }
        }
            steps {
                echo " excute all"
            }
        stage ('prod'){
            steps{
                echo " deploying to prod"
            }
        }
        }
    }
