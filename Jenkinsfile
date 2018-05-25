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
		       subject: "Job Build", 
		       body: "Job Build Success.${env.JOB_NAME} [${env.BUILD_NUMBER}]",
		       to: "badal.singh2432@gmail.com,rishulasinha13@gmail.com"
		     )
		    }
	    }
    }
}
