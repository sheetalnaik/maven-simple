pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
            git url: 'https://github.com/sheetalnaik/Newrepo.git/'
         }
      }
   
   
      stage('Hi') {
         steps {
            buildInfo = rtMaven.run pom: 'maven-example/pom.xml', goals: 'clean install'
         }
      }
   
 
      
   }
}
