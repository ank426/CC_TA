pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES1UG22CS098-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        // echo 'deploy'
        false
      }
    }
  }
  post {
    failure {
      error "Pipeline failed"
    }
  }
}
