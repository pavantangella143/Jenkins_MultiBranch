node('master')

{

stage('Continuous Download') 
   
	 {
	
    git 'https://github.com/sunildevops77/maven.git'
    
	}

stage('Continuous build') 
   
	 {
	
   sh label: '', script: 'mvn package'
	}

stage('Continuous Deployment') 
   
	 {
	
 sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war  ubuntu@172.31.34.24:/var/lib/tomcat8/webapps/qaenv.war'
	}
}

