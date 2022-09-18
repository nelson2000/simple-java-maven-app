pipeline{

	agent {   
		docker {
			image 'maven:openjdk:11-jdk'
			args '-v /root/.m2:/root/.m2'
			}

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
