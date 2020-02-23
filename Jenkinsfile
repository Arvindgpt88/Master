node {
     
   stages {  
 	     
    stage('SCM Checkout'){
    // Clone repo
             
           git branch: "${params.Branch}", 
           url: 'https://github.com/Arvindgpt88/Master.git' 
        }     
	
   stage('Ok') {
                echo "Ok"
            }
   }
 
    post {
        always {
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'aravindgpt88@gmail.com']], subject: 'Jenkins Build'
								
	}								
 }
}

