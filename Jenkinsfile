pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git branch: 'main', url: 'https://github.com/bbssmile/WebGoat.git'
      }
    }
    stage('Clone') {
      steps {
        withDockerRegistry(url: 'https://index.docker.io/v1/') {
            sh 'docker build -t bbssmile/WebGoat:v10'
            sh 'docker push -t bbssmile/WebGoat:v10'
        }
      }
    }
  }
}
