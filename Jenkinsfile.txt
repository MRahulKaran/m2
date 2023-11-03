pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        maven 'clean compile'
      }
    }
    stage('Test') {
      steps {
        maven 'test'
      }
    }
    stage('Deploy') {
      steps {
        maven 'deploy'
      }
    }
  }
}