pipeline {
    agent any
    tools {
	go 'Golang version 17.3'
    }
    stages {
	stage('compile and test') {
	    agent {
		dockerfile {
		    filename 'Dockerfile.build'
		}
	    }
	    steps {
		sh 'cd hypernyms ; go build'
		sh './hypernyms/hypernyms'
		archiveArtifacts artifacts: 'hypernyms/hypernyms', fingerprint: true
	    }
	}
    }
}
