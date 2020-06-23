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
		    sh "eval 'ssh-agent -s' && ssh-add ${KEY_FILE}"	    
            sh 'ls'
	    sh 'whoami'
            sh 'pwd'
            }
            }
        }
	    
	  
    }
}
