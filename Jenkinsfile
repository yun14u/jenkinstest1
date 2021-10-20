pipeline{

        agent {label 'asrock'}

        stages {
            
            stage('alpha') {
                        when {
                               expression { env.BRANCH_NAME == "origin/alpha" }                            
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
                            allOf {
                               expression { env.BRANCH_NAME == "origin/main" }
                               expression { params.merged == true }
                               expression { params.current_status == "closed" }
                            }
                        }
                        steps {
                                sh 'echo prod !!! '
                        }
                }

        }

}
