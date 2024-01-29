pipeline {
  agent {
    label 'buildnode'
  } 
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
    disableConcurrentBuilds()
  }
  stages {
    stage('Hello') {
      steps {
        sh 'echo "Hello"'
      }
    }
    stage('cat README') {
      when {
        branch "*1"
      }
      steps {
        sh '''
          cat README.md
        '''
      }
    }
  }
}
