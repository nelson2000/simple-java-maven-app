pipeline {
  agent {
    node {
      label 'Node3'
    }

  }
  stages {
    stage('CodeBuild') {
      steps {
        sh 'echo This is the code build stage'
        sh 'mvn package'
      }
    }

    stage('CodeTest') {
      steps {
        sh 'echo This is the code test stage'
      }
    }

    stage('CodePlay') {
      parallel {
        stage('CodePlay') {
          steps {
            echo 'The end'
          }
        }

        stage('codeslay') {
          steps {
            echo 'Thank you'
          }
        }

      }
    }

  }
  tools {
    maven 'maven38'
  }
}