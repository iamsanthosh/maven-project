pipeline {
    agent any
	stages {
	    stage('Build') {
    	   steps {
   	        sh 'mvn clean package'
   	        sh "sudo usermod -a -G docker $USER"
   	        sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"   	        
   	    	}
    	}
	}
}
