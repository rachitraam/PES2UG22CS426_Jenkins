pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG22CS426-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './ouput'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      error 'Pipeline Failed'
    }
  }
}
