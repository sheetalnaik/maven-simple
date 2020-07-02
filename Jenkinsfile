pipeline {
   agent any

   stages {
      stage('checkout') {
         steps {
             git url: 'https://github.com/sheetalnaik/Newrepo.git'
         }
      }
   
   
      stage('build') {
         steps {
           sh 'mvn clean package'
         }
      }
      
   }
}
