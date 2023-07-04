pipeline {
	agent any

	options {
		disableConcurrentBuilds()
	}

	stages {
		stage('Hello') {
			steps {
				echo 'Hello'
			}
		}
		stage('for the fix branch') {
			when {
				branch 'fix-*'
			}
			steps {
				sh 'cat README.md'
			}
		}
		stage('for the PR') {
			when {
				branch 'PR-*'
			}
			steps {
				echo 'This runs only for the PRs'
			}
		}
	}
}
