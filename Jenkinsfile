pipeline{

        agent {label 'asrock'}
        triggers {
            GenericTrigger(
               genericVariables: [
                [key: 'ref', value: '$.ref'],
                [key: 'merged', value: '$.merged'] 
               ]
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
                                sh 'echo merged $merged'
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
