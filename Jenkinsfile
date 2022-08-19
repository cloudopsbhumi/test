pipeline {
  agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage('checkout') {
	      
            steps {
                
                git branch: 'main', url: 'https://github.com/arsh-ash/Portfolio-website.git'
			    stash 'source'
			    echo 'stash is successfull'
            }
        }
        stage('build npm') {
            steps {
                unstash 'source'
                echo 'unstash is successfull'
               
            }
	}
        
    }
}
