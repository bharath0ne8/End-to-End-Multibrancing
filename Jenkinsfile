pipeline {
  agent any

  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
  }

  stages {
    stage('Hello') {
      when {
        branch "main"
      }
      steps {
        sh '''
          java -version
        '''
      }
    }

    stage('main branch') {
      when {
        branch "main"
      }
      steps {
        sh '''
          echo "This is the main branch"
        '''
      }
    }
  }
}

