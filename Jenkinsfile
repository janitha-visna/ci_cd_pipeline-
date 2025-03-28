pipeline {
  agent {
    docker {
      image 'node:18' // ✅ Use Node.js image instead of installing npm
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
        sh 'npm install'  // ✅ No sudo needed
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

