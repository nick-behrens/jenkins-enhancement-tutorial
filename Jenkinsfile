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
                        script: "curl https://raw.githubusercontent.com/pi314/ascii-arts/master/octocat.asciiart",
                        returnStdout: true
                    ).trim()
                    println "${gitBranch}"
                }
            }
        }
    }
}
