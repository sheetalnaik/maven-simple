pipeline {
   agent any

   stages {
      stage('Clone sources') {
        git url: 'https://github.com/sheetalnaik/Newrepo.git/'
    }
      
   
   
      stage('Maven build') {
        buildInfo = rtMaven.run pom: 'maven-example/pom.xml', goals: 'clean install'
    }
   
 
     
   }
}
