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
        stage ('second stage') {
            steps {
                echo " excute all"
            }
        stage ('prod'){
            when {
                buildingTag()
            }
            steps{
                echo " deploying to prod"
            }
        }
        }
    }

}
