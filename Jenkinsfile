pipeline{

        agent {label 'asrock'}


        stages {
            
            stage('gitclone') {
                        steps {
                               sh 'echo gitclone - use git '
                        }
                }

                stage('Build') {
                        steps {
                                sh 'echo docker build '
                        }
                }

                stage('Login') {
                        steps {
                                sh 'echo DOCKERHUB_CREDENTIALS_PSW to docker login '
                        }
                }

                stage('Push') {

                        steps {
                                sh 'echo docker push'
                        }
                }
        }

}