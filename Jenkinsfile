pipeline {
    agent any
	
    stages {
        stage('Compile') {
            steps {
                bat 'set path ="C:\Program Files\Java\jdk1.8.0_171\bin"'
            }
        }
        stage('Run') {
            steps {
                bat "javac Hello.java & java Hello"
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
