pipeline{
    agent any
    parameters {
        booleanParam (
            name: 'SRE_APPROVED',
            defaultValue: true,
            description: 'Is SRE approval taken for this release'
        )
        choice (
            choices: 'Regular\nHotfix',
            description: "What sort of release is this, regulare release or hotfix ?" 
            name: 'Release'
        )
        text (
            name: 'Notes',
            defaultValue: "Enter Release notes",
            description: "Do enter the description" 
        )
        credentials ( 
            name: 'mycrediantials',
            description: "myCredentials",
            required: true
        )
    stages {
        stage ('first stage') {
            steps {
                echo " approval parameter ${params.SRE_APPROVED}"
                echo " Release parameter ${params.Release}"
                echo "Notes parameter ${params.Notes}"
                 echo "mycrediantials parameter ${params.mycrediantials}"

            }
        }
    }
    }
}
