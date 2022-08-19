pipeline {
  agent any
    stages {
        stage('checkout') {
	     agent { 
    		label 'jenkins-agent'
		}
            steps {
		git branch: 'main', url: 'https://github.com/mangesh16cloud/jenkinspipeline.git'
		stash 'source'
		echo 'stash successful'
            }
        }
	
        stage('build') {
	    
            steps {
		unstash 'source'
                echo 'Hello World'
            }
        }
    }
}
