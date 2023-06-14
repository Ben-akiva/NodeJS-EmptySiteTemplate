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
        sh '''npm install
npm run start &'''
      }
    }

    stage('test') {
      steps {
        sh 'curl localhost:8080'
      }
    }

    stage('package') {
      steps {
        sh 'tar czvf nodeejs.tar.gz *'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '*.tar.gz'
      }
    }

  }
}