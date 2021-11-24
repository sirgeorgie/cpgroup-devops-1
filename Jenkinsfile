pipeline {
    agent any
    tools {
	go 'Golang version 1.17.3'
    }
    stages {
	stage('compilation') {
	    steps {
		sh 'go build synonyms.go'
	    }
	}
    }
    post {
	always {
	    archiveArtifacts artifacts: 'synonyms', fingerprint: true
	}
    }
}
