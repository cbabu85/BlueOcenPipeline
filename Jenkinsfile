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
            publishCoverage(calculateDiffForChangeRequests: true, failBuildIfCoverageDecreasedInChangeRequest: true, failNoReports: true, failUnhealthy: true, failUnstable: true, applyThresholdRecursively: true)
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