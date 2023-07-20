pipeline {
    agent any 
    environment {
        DEPLOY_TO = "SIVA"
    }
    stages {
        stage ("deploy") {
            when {
              allOf {
                branch 'production'
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
        }
    }

}
