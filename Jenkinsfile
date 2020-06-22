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
    }
}
