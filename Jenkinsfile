pipeline {
   agent any

   stages {
   
		stage('Push a container'){
			steps {
				dir('azure-vote/') {
					script{
						docker.withRegistry('https://index.docker.io/v1/', 'DockerHub'){
								def image = docker.build('akshatparikh/jenkins_demo:latest')
								image.push()
						}
					}
				}
			}
		}
      
      //stage('Docker Build') {
      //   steps {
      //      dir('azure-vote/') {
      //          bat 'docker build -t jenkins-pipeline .'
      //      }
      //   }
		// post {
		//	success{
		//		echo ('The run is a success')
		//	}
		//	failure{
		//		echo ('The run is a failure')
		//	}
		// }
      //}
   }
}