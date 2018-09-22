pipeline {
  agent {
    node {
      label 'Maven 3.4.5'
    }

  }
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