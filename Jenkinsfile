pipeline{

        agent {label 'asrock'}
        stages {
            
            stage('alpha') { 
                        steps {
                               sh 'GIT_BRANCH $GIT_BRANCH '
                        }
                }

                stage('uat') {
                        when {
                               expression { env.BRANCH_NAME == "origin/uat" }                            
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
