pipeline {
  agent any
  options {
    buildDiscarder logRotator(artifactDays: '', artifactNumberToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
    disableConcurrentBuilds()
  }
  stages {
    stage('Hello') {
      steps {
        sh 'echo "Hello"'
      }
    }
  }
}
