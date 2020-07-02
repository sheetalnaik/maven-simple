pipeline {
   agent any

   stages {
      stage('checkout') {
         steps {
             git url: 'https://github.com/sheetalnaik/ssn_sample_git_pjct.git'
         }
      }
   
   
      stage('build') {
         steps {
           sh 'clean package'
         }
      }
      
   }
}
