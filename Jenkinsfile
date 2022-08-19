pipeline {
  agent any
    stages {
        stage('SCM checkout') {
	     agent { 
    		label 'jenkins-agent'
		}
            steps {
		git branch: 'main', url: 'https://github.com/arsh-ash/Portfolio-website.git'
		stash 'source'
		echo 'stash successful'
            }
        }
	
        stage('npm build') {
	    
            steps {
		unstash 'source'
                echo 'unstash successful'
            }
        }
    }
}
