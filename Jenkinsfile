pipeline {
  // agent { docker { image 'python:3.7.2' } }
  agent {label `main-host`}
  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', credentialsId: '1889a3a3-80f8-4bb4-b656-f67f52fe11d8',url: 'git@github.com:egolinko/qgel.git'
      }
      }
    stage('test') {
      steps {
        sh 'python test.py'
      }
    }
  }
}
