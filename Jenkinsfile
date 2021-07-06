pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'mvn clean package'
          }
        }

        stage('Test') {
          steps {
            echo 'Print Test'
            sh 'mvn clean test'
            publishCoverage()
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Print Deploy'
      }
    }

  }
  environment {
    Maven = 'opt/maven'
  }
}