pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Build Java Application '
          }
        }

        stage('Test') {
          steps {
            echo 'Testing the Application'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy to Some Server'
      }
    }

  }
}