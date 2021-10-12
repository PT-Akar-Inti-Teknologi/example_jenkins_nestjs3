pipeline {
  agent any

  stages {
    stage('Build & Test') {
      agent {
        docker {
          image 'node:14.17.0-alpine'
          reuseNode true
        }
      }
      steps {
        sh 'yarn test:cov'
      }
    }
  }
}
