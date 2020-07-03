pipeline {
   agent any

   stages {
      stage('Git checkout') {
         steps {
             git url: 'https://github.com/sheetalnaik/Newrepo.git'
         }
      }
   
   
      stage('Maven build') {
         steps {
           sh 'mvn clean package'
         }
      }
      stage("Publish to Nexus Repository") {
         steps {
                        nexusArtifactUploader artifacts: [
	[
		artifactId: 'hello-world-war', 
		classifier: '', 
		file: 'target/hello-world-war-1.0.0.war', 
		type: 'war'				]
	], 
		credentialsId: 'nexus', 
		groupId: 'com.efsavage', 
		nexusUrl: 'localhost:8081', 
		nexusVersion: 'nexus3', 
		protocol: 'http', 
		repository: 'newnexusrepo', 
		version: '1.0.0'		

	     }
       } 
   }
}
