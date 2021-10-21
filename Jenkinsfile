pipeline{

        agent {label 'asrock'}
        triggers {
            GenericTrigger(
               genericVariables: [
                [key: 'ref', value: '$.ref'],
                [key: 'merged', value: '$.merged'] 
               ],
                causeString: 'Triggered on $ref',

               token: '',
               tokenCredentialId: '',

               printContributedVariables: true,
               printPostContent: true,

               silentResponse: false,

               regexpFilterText: '$ref',
               regexpFilterExpression: 'refs/heads/' + BRANCH_NAME
            )
        }
        stages {
            
            stage('alpha') { 
                        when {
                              branch 'alpha'                           
                        }
                        steps {
                                sh 'echo alpha !'
                                sh 'echo ref $ref'
                        }
                }

                stage('uat') {
                        when {
                               branch 'uat'                          
                        }
                        steps {
                                sh 'echo uat !!'
                                sh 'echo ref $ref'
                        }
                }

                stage('prod') {
                        when {
                               branch 'main'
                        }
                        steps {
                                sh 'echo prod !!! '
                        }
                }

        }

}
