pipeline {
   agent any

   stages {
      
      stage('Docker Build') {
         steps {
            dir('azure-vote/') {
                bat 'docker images -a'
                bat 'docker build -t jenkins-pipeline .'
            }
         }
      }
   }
}