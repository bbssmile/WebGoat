pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git branch: 'main', url: 'https://github.com/bbssmile/WebGoat.git'
      }
    }
    stage('build') {
      steps {
        withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1/') {
            sh 'docker build -t bbssmile/WebGoat:v10'
            sh 'docker push -t bbssmile/WebGoat:v10'
        }
      }
    }
  }
}
