/* groovylint-disable CompileStatic, NestedBlockDepth */

pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                script {
                    if (env.CHANGE_ID) {
                        echo "Build running for PR $pullRequest.number: $pullRequest.url"
                    } else {
                        echo "Build running for branch: $env.BRANCH_NAME"
                    }
                    sleep 30
                    if (env.CHANGE_ID) {
                        pullRequest.comment('test')
                    }
                }
            }
        }
    }
}
