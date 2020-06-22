 pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
            echo 'Deploying....'
            sshagent(credentials: ['ec2-appServer']) {
            sh 'ls'    
	    sh 'pwd'	    
	      	      
             }
            }
        }
	    
	    stage('ssh pipeline'){
		 steps{
		def remote = [:]
  	    remote.name = 'AWS'
  	    remote.host = 'ec2-3-25-98-11.ap-southeast-2.compute.amazonaws.com'
  	    remote.user = 'ec2-user'
  	    remote.password = ''
  	    remote.allowAnyHosts = true	    
		 sshCommand remote: remote, command: "ls -la"   
		    }
            }
    }
}
