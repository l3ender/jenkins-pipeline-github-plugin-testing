/* groovylint-disable CompileStatic, NestedBlockDepth */

pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                script {
                    sh 'printenv'
                    echo "pr detected? $env.CHANGE_ID"
                    if (env.CHANGE_ID) {
                        echo "PR: $pullRequest.number"
                    } else {
                        echo 'no PR'
                    }
                }
            }
        }
    }
}
