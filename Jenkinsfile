pipeline{

	agent {   
		docker {
			image 'maven:openjdk:11-jdk'
			args '-v /root/.m2:/root/.m2'
			}

		}

    stages{

      stage('CodeCheckout'){
	
		steps{
			sh 'echo This is the code checkout stage'
			checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'git-cred', url: 'https://github.com/nelson2000/simple-java-maven-app.git']]])

			}


	}


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
