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
                    gitBranch = sh(
                        script: "echo hello",
                        returnStdout: true
                    ).trim()
                    println "${gitBranch}"
                }
            }
        }
    }
}
