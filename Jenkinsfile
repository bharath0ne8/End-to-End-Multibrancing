pipeline {
    agent any

    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
    }

    triggers {
        // Trigger the pipeline only for the "dev" branch
        branch('dev')
    }

    stages {
        stage('Hello') {
            steps {
                sh '''
                    java -version
                '''
            }
        }

        stage('cat README') {
            steps {
                sh '''
                    cat README.md
                '''
            }
        }
    }
}

