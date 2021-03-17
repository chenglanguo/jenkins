def scmVars
pipeline {
  agent any
  options {
    preserveStashes(buildCount: 5)
  }

  environment {
              scmVars = checkout([
            $class: "GitSCM",
            userRemoteConfigs: [[credentialsId: "personal-git", url: "https://github.com/chenglanguo/app.git"]]
          ])
  }
  stages {
    stage('checkout') {
      steps {
        script {
          // scmVars = checkout([
          //   $class: "GitSCM",
          //   userRemoteConfigs: [[credentialsId: "personal-git", url: "https://github.com/chenglanguo/app.git"]]
          // ])
          echo "${scmVars}"
        }

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
          git_hash = "${scmVars}"
        }
        echo "${git_hash}"
        echo "hahaha"
        echo "commit"
        // sh "env"
      }
    }
  }
}