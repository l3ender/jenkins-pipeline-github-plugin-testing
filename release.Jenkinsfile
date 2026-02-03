/* groovylint-disable CompileStatic, NestedBlockDepth */

pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                script {
                    if (mergedPullRequest.exists) {
                        echo "PR was merged: $mergedPullRequest.number"
                    } else {
                        echo 'no PR'
                    }
                }
            }
        }
    }
}
