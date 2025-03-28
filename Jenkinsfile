pipeline {
  agent {
    dockerContainer {
      image 'node:18' // ✅ Corrected agent type
    }
  }
  stages {
    stage("Checkout") {
      steps {
        checkout scm
      }
    }
    stage("Test") {
      steps {
        sh 'npm install'
        sh 'npm test'
      }
    }
    stage("Build") {
      steps {
        sh 'npm run build'
      }
    }
  }
}
