pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'mvn clean install -Dlicense.skip=true'
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