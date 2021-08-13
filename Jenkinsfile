pipeline {
  agent {
    node {
      label 'centos7-nodejs2'
    }

  }
  stages {
    stage('check out Code') {
      steps {
        git(url: 'https://github.com/razorbach1/NodeJS-EmptySiteTemplate.git', branch: 'master', changelog: true, poll: true)
      }
    }

    stage('Build & Compile') {
      steps {
        sh 'npm install'
      }
    }

    stage('test Code') {
      steps {
        sh '''node server.js
curl localhost:8080
if [[ "x$?" == "x0" ]]; 
then    echo good; 
else exit 1; 
fi'''
      }
    }

  }
}