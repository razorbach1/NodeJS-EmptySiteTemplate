pipeline {
  agent any
  stages {
    stage('check out Code') {
      steps {
        git(url: 'https://github.com/razorbach1/NodeJS-EmptySiteTemplate.git', branch: 'master', changelog: true, poll: true)
      }
    }

  }
}