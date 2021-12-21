pipeline {
  agent any
  stages {
    stage('feature') {
      when {
        expression {
          return env.GIT_BRANCH == "origin/feature"
        }
      }
      steps {
        sh """
        echo "Building  Artifacts on Feature"
        """
      }
    }
    stage('Deploy Code') {
      when {
        expression {
          return env.GIT_BRANCH == "origin/main"
        }
      }
      steps {
        sh """
        echo "Deploying Code on Main"
        """
      }
    }
  }
}
