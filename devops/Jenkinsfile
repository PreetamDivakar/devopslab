pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Run BlueWave script') {
      steps {
        sh 'chmod +x hello-world.sh || true'
        sh './hello-world.sh'
      }
    }
  }
  post {
    success { echo 'Pipeline finished SUCCESS' }
    failure { echo 'Pipeline FAILED' }
  }
}
