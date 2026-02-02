/* groovylint-disable CompileStatic, NestedBlockDepth */

pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                script {
                    sh 'printenv'
                    if (env.mergedPullRequest) {
                        echo "PR was merged: $mergedPullRequest.number"
                    } else {
                        echo 'no PR'
                    }
                }
            }
        }
    }
}
