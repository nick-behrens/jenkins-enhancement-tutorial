library "jenkins-library@no-ref-nick-jenkins-tutorial"

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
