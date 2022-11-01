library "jenkins-library"
def autoCancelled = false
CRON_SETTINGS = "${env.BRANCH_NAME}" == "develop" ? '''0 18 1-7,15-21 * 1 %CRON_TYPE=RELEASE
                                                       0 0 * * 1-5 %CRON_TYPE=NIGHTLY''' : ""

def helmEnvs = [""]
def helmEnv = ""
def directory = ''
def gitRepoUrl = "https://github.com/snapdocs/rumi-reporting"

pipeline {
    triggers {
        parameterizedCron(CRON_SETTINGS)
    }
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
