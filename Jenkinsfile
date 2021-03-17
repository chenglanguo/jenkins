pipeline {
  agent any
  options {
    preserveStashes(buildCount: 5)
  }
  stages {
    stage('build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
      }
    }
    stage('Deploy-change') {
      steps {
        echo 'Deploying...-hhh'
      }
    }
  }
}