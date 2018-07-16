pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 4000:3000 -u root'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh ' sh \'npm install\''
      }
    }
  }
}