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
	
   stage('Maven Clean Package'){
	 steps{   
	    bat "${mvnhome}/bin/mvn clean package"
	}
     }
 
   stage('IP CONFIG'){
	 steps{
	    bat "ipconfig"
	 }
     }
    post {
        always {
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'arvindgpt88@gmail.com']], subject: 'Jenkins Build'
								
	}								
 }
}
}
