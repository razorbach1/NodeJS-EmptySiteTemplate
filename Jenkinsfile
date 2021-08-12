pipeline {
  agent {
    node {
      label 'entos7-nodejs'
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

  }
}