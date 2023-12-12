pipeline {
  agent any

  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
  }

  stages {
    stage('Test branch') {
      when {
        branch "test"
      }
      steps {
        sh '''
          echo "This is the test branch"
        '''
      }
    }
  }
}

