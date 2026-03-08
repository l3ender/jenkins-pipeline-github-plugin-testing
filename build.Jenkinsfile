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
                    if (mergedPullRequest.exists) {
                        echo "Merged PR detected: $mergedPullRequest.number"
                    } else {
                        echo 'No merged PR detected'
                    }
                }
            }
        }
    }
}
