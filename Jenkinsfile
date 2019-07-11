pipeline {
  agent {
    node {
      label 'jenkins'
    }

  }
  stages {
    stage('Configure') {
      steps {
        echo 'Hello'
        sh '''#!/bin/sh
ls -la
'''
      }
    }
  }
}