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
    stage('Deploy-change-name') {
      steps {
        script {
          git_hash = sh(script: "git log -n 1 --pretty=format:'%h'", returnStdout: true).trim()
        }
        echo "${git_hash}"
        echo "hahaha"
        // sh "env"
      }
    }
  }
}