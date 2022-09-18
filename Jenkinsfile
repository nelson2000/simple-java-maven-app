pipeline{

	agent any
	
	tools {
	       maven 'maven38'
	}
    stages{

     stage('CodeBuild'){

                steps{
                        sh 'echo This is the code build stage'
			sh 'mvn package'
                        
                        }

		}

     stage('CodeTest'){

                steps{
                        sh 'echo This is the code test stage'

                        }

		}


     
}



}
