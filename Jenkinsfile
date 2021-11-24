pipeline {
    agent any
    stages {
		stage('compilation') {
			steps {
				sh 'go build synonyms.go'
			}
		}
    }
}
