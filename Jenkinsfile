pipeline {
  agent any
  stages {
    stage('Install UTILITIES') {
      steps {
        echo 'This is install Utilities'
        sh '''unzip -o utilities.zip
chmod +x ./install.sh
./insatll.sh'''
        pwd(tmp: true)
      }
    }
    stage('Install PF') {
      steps {
        echo 'This is to install PF'
        archiveArtifacts(allowEmptyArchive: true, caseSensitive: true, defaultExcludes: true, artifacts: '/tmp', onlyIfSuccessful: true, excludes: '/*.zip')
      }
    }
  }
  environment {
    SHELL = 'bash'
    USER = 'netcrk'
  }
}