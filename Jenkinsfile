pipeline {
  agent any
  stages {
    stage("checkout") {
      steps {
        checkout scm
      }
    }
    stage("Test") {
      steps {
        sh 'sudo npm install'  // ❌ Possible error
        sh 'npm test'
      }
    }
    stage("Build") {
      steps {
        sh 'npm run build'
      }
    }
  }  // ✅ Missing closing bracket added here
}
