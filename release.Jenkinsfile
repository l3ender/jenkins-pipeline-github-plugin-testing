/* groovylint-disable CompileStatic, NestedBlockDepth */

pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                script {
                    sh 'printenv'
                    echo "merge detected? $env.GITHUB_PR_MERGE_DETECTED"
                    if (env.GITHUB_PR_MERGE_DETECTED) {
                        echo "PR was merged: $mergedPullRequest.number"
                    } else {
                        echo 'no PR'
                    }
                }
            }
        }
    }
}
