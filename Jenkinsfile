pipeline {
    agent any
	
    stages {
        stage('Compile') {
            steps {
                bat "javac Hello.java"
            }
        }
        stage('Run') {
            steps {
                bat "java Hello"
            }
        }
	    stage('emailNotification'){
		    steps{
			    emailext ( 
		       subject: "Subject", 
		       body: "${env.JOB_NAME} [${env.BUILD_NUMBER}]':",
		       to: "edara.nagasamyuktha@gmail.com,rishulasinha13@gmail.com"
		     )
		    }
	    }
    }
}
