pipeline {
   agent any

   stages {
      
      stage('Docker Build') {
         steps {
            dir('azure-vote/') {
                bat 'docker build -t jenkins-pipeline .'
            }
         }
		 post {
			success{
				echo ('The run is a success')
			}
			failure{
				echo ('The run is a failure')
			}
		 }
      }
   }
}