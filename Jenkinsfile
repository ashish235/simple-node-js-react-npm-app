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
        sh 'npm install'
      }
    }
    stage('Deliver') {
      steps {
        sh './jenkins/scripts/deliver.sh'
        input 'Finished using the web site?'
        sh './jenkins/scripts/kill.sh'
      }
    }
  }
}