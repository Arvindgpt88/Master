properties([parameters([choice(choices: 'master\npipeline\nnew-branch\nStore_varable', name: 'Branch')])])

node{
	
       def mvnhome = tool name: 'Maven', type: 'maven'
	def dockerImage
       tool name: 'DOCKER_TOOLBOX_INSTALL_PATH', type: 'org.jenkinsci.plugins.docker.commons.tools.DockerTool'
    stage('SCM Checkout'){
    // Clone repo
	    git branch: "${params.Branch}", 
	url: 'https://github.com/Arvindgpt88/Master.git' 
 }
	
 stage('Maven Clean Package'){
	 bat "${mvnhome}/bin/mvn clean package"
	
 }
 
 stage('IP CONFIG'){
	 def ip = C:\Windows\System32\cmd.exe
	 bat "$(C:\Windows\System32\cmd.exe)\ipconfig"
 }

}

