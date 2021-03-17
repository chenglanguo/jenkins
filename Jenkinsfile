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
        scripts {
          def git_hash = $BUILD_NUMBER
        }
        echo ${git_hash}
      }
    }
  }
}