 pipeline {
    agent any
 environment {
        KEY_FILE = '/home/jenkins/appServer.pem'
    }
	 
    stages {
        stage('Deploy') {
            steps {
            echo 'Deploying....'
	    withCredentials([sshUserPrivateKey(credentialsId: 'ec2-appServer', keyFileVariable: 'KEY_FILE')]) {
	    sh 'ssh-agent bash'
	    sh 'ssh-add ${KEY_FILE}'	    
	    sh 'ssh -A ec2-user@3.25.98.11 -y'	        
            sh 'ls'
	    sh 'whoami'
            sh 'pwd'
            }
            }
        }
	    
	  
    }
}
