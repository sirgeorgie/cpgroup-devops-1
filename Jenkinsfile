pipeline {
    agent any
    tools {
	go 'Golang version 17.3'
    }
    stages {
	stage('compilation') {
	    steps {
		sh 'go build synonyms.go'
	    }
	}
    }
}
