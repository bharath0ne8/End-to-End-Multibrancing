pipeline {
    agent any

    options {
        buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5'))
    }

    triggers {
        pollSCM('*/5 * * * *')  // Poll SCM every 5 minutes
    }

    stages {
        stage('Hello') {
            steps {
                sh 'java -version'
            }
        }

        stage('cat README') {
            steps {
                sh 'cat README.md'
            }
        }
    }
}

