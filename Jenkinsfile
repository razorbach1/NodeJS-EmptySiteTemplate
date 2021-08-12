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
        cleanWs(cleanWhenAborted: true, cleanWhenFailure: true, cleanWhenSuccess: true)
      }
    }

    stage('Build & compile') {
      steps {
        sh 'npm install'
      }
    }

    stage('packege code') {
      steps {
        sh 'tar -czvf.node.tar.gz .'
      }
    }

  }
}