pipeline{

        agent {label 'asrock'}
        stages {
            
            stage('alpha') { 
                        when {
                               expression { env.GIT_BRANCH == "origin/alpha" }                            
                        }
                        steps {
                               sh 'echo alpha ! '
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
