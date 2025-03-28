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
        sh 'sudo apt install npm'  // ❌ Possible error
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
