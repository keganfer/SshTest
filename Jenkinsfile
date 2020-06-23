 pipeline {
    agent any
 environment {
        KEY_FILE = '/home/jenkins/appServer.pem'
    }
	 
    stages {
        stage('Deploy') {
            steps {
            echo 'Deploying....'
	    
	    sh 'ssh-agent > script.sh && source script.sh && rm script.sh && ssh-add ${KEY_FILE} && ssh -A ec2-user@3.25.98.11 -y'	        
            sh 'ls'
	    sh 'whoami'
            sh 'pwd'
            
            }
        }
	    
	  
    }
}
