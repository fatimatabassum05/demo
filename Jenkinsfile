pipeline{
	agent any
	parameters {
		choice(name: 'DEPLOY_TO', choices: ['DEV', 'QA', 'PROD'])
	}
	triggers {
		githubPush()
	}
	stages {
		stage('Checkout') {
			steps {
        echo "Checkout completed"
			}
		}

		stage('Test') {
			steps {
				echo "Running static tests on code"
			}
		}

		stage('Build') {
      			when {
        			branch "main"
      			}
			steps {
				sh 'echo "Building the code"'
			}
		}

		stage('Deploy') {
			steps {
				echo "deploying into environment"
			}
		}

	}
}
