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
                               branch 'main'
                        }
                        steps {
                                sh 'echo prod !!! '
                        }
                }

        }

}
