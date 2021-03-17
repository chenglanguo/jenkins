pipeline {
  agent any
  options {
    preserveStashes(buildCount: 5)
  }
  stages {
    stage('checkout') {
      steps {
        echo 'checkout...'
      }
    }
    stage('build') {
      steps {
        echo 'building...'
      }
    }
    stage('Deploy') {
      steps {
        script {
          git_hash = "${GIT_COMMIT}"
        }
        echo "${git_hash}"
        echo "hahaha"
        echo "commit"
        // sh "env"
      }
    }
  }
}