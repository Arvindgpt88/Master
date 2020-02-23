node {
 	     
    stage('SCM Checkout'){
    // Clone repo
             
           git url: 'https://github.com/Arvindgpt88/Master.git' 
        }     
	
   stage('Ok') {
                echo "Ok"
            }
 
    /*post {
        always {
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'aravindgpt88@gmail.com']], subject: 'Jenkins Build'
								
	}*/								
	
   stage('Email'){
	   emailext (
    			subject: "Job '${env.JOB_NAME} ${env.BUILD_NUMBER}'",
    			body: """<p>Check console output at <a href="${env.BUILD_URL}">${env.JOB_NAME}</a></p>""",
    			to: "aravindgpt88@gmail.com",
 			)
}
}
