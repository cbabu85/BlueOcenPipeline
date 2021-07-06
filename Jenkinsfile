pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh '"./mvnw clean install -DskipTests"'
          }
        }

        stage('Test') {
          steps {
            echo 'Print Test'
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
}