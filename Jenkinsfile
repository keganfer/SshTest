 pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
            echo 'Deploying....'
	    withCredentials([sshUserPrivateKey(credentialsId: 'ec2-appServer', keyFileVariable: '/home/jenkins/appServer.pem')]) {
	    sh "eval 'ssh-agent -s' && ssh-add /home/jenkins/appServer.pem"	    
            sh 'ls'
	    sh 'whoami'
            sh 'pwd'
            }
            }
        }
	    
	  
    }
}
