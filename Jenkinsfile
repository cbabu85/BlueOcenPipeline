pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            build 'pom.xml'
          }
        }

        stage('Test') {
          steps {
            echo 'Print Test'
          }
        }

      }
    }

  }
}