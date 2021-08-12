pipeline {
  agent {
    node {
      label 'centos7-nodejs'
    }

  }
  stages {
    stage('Check Out Code') {
      steps {
        git(url: 'https://github.com/razorbach1/NodeJS-EmptySiteTemplate.git', branch: 'master', changelog: true, poll: true)
      }
    }

    stage('Build & compile') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test Code') {
      steps {
        sh '''node server.js &
 sleep 5 &&
curl localhost:8081 
if [[ "x$?" == "x0" ]];
then    echo good;
else exit 1; 
fi'''
      }
    }

  }
}