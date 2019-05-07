pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Install Testcafe') {
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
