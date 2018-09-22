pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'mvn clean package'
          }
        }
        stage('Package') {
          steps {
            sh 'mvn clean install'
          }
        }
      }
    }
  }
}