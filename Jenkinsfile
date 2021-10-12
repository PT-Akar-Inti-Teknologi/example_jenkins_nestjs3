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
        sh 'yarn install'
        sh 'yarn test:cov'
      }
    }

    stage('Coding Standard') {
      agent {
        docker {
          image 'node:14.17.0-alpine'
          reuseNode true
        }
      }
      steps {
        sh 'yarn lint:test'
      }
    }
  }
}
