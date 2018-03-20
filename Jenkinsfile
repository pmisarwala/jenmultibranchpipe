pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        echo 'Hello Dear and Dear'
      }
    }
    stage('Build') {
      steps {
        sh 'echo \'This is a build stage\''
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'echo \'First Test Execution\''
          }
        }
        stage('Unit Test') {
          steps {
            sh 'echo \'Second Test Execution\''
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        sh 'This is deploy stage'
      }
    }
  }
}