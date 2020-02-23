pipeline {
   agent any
  
   stages {  
 	     
    stage('SCM Checkout'){
    // Clone repo
        steps{     
           git branch: "${params.Branch}", 
           url: 'https://github.com/Arvindgpt88/Master.git' 
        }
     }	     
	
   stage('Ok') {
            steps {
                echo "Ok"
            }
        }
   }
 
    post {
        always {
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'aravindgpt88@gmail.com']], subject: 'Jenkins Build'
								
	}								
 }
}

