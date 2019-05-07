pipeline {
  agent any
  stages {
    stage('Install Testcafe') {
      stage('Build') {
      steps {
        sh 'npm install'
      }
      steps {
        sh 'npm install testcafe testcafe-reporter-xunit'
      }
    }
    stage('Run TestCafe') {
      steps {
        sh 'node_modules/.bin/testcafe chrome tests/**/* -r xunit:res.xml'
      }
    }
  }
}
