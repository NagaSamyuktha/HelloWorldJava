pipeline {
    agent any
	
    stages {
        stage('Hello') {
            steps {
                bat 'echo "Hello"'
            }
        }
	    stage('emailNotification'){
		    steps{
			    emailext ( 
		       subject: "Subject", 
		       body: "${env.JOB_NAME} [${env.BUILD_NUMBER}]",
		       to: "edara.nagasamyuktha@gmail.com,rishulasinha13@gmail.com"
		     )
		    }
	    }
    }
}
