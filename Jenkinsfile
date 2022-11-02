library "jenkins-library"

pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5', artifactNumToKeepStr: '5'))
    }
    stages {
        stage('print art'){
            steps {
                script {
                    github.octocatComment()
                }
            }
        }
    }
}
