pipeline {
  agent {
    node {
      label 'docker'
    }

  }
  stages {
    stage('chekout') {
      steps {
        git(url: 'https://github.com/Ben-akiva/NodeJS-EmptySiteTemplate.git', branch: 'master')
      }
    }

    stage('build') {
      steps {
        sh 'npm install'
      }
    }

  }
}