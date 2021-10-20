pipeline{

	agent {label 'asrock'}

	stages {
	    when {
            allOf {
               expression { env.BRANCH_NAME == "origin/uat" }
               expression { params.merged == true }
               expression { params.current_status == "closed" }
            }
        }

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
