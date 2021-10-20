pipeline{

        agent {label 'asrock'}
        stages {
            
            stage('alpha') { 
                        when {
                              branch 'alpha'                           
                        }
                        steps {
                                sh 'echo alpha !'
                        }
                }

                stage('uat') {
                        when {
                               branch 'uat'                          
                        }
                        steps {
                                sh 'echo uat !!'
                        }
                }

                stage('prod') {
                        when {
                               expression { env.BRANCH_NAME == "origin/main" }
                        }
                        steps {
                                sh 'echo prod !!! '
                        }
                }

        }

}
