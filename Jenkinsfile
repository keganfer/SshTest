 pipeline {
    agent any
 environment {
        KEY_FILE = '/home/jenkins/appServer.pem'
    }
	 
    stages {
        stage('Deploy') {
            steps {
            echo 'Deploying....'
	    bash '/home/jenkins/appServer.sh'     
 	    echo 'second'
	    sh 'whoami'	    
            
            }
        }
	    
	  
    }
}
