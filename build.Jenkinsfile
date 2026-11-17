/* groovylint-disable CompileStatic, NestedBlockDepth */

pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                script {
                    if (env.CHANGE_ID) {
                        echo "adding comment to PR before sleep"
                        pullRequest.comment("Comment from build before sleep: ${new Date().format('yyyy-MM-dd HH:mm:ss z')}")
                    }
                    sleep 30
                    if (env.CHANGE_ID) {
                        echo "adding comment to PR after sleep"
                        pullRequest.comment("Comment from build after sleep: ${new Date().format('yyyy-MM-dd HH:mm:ss z')}")
                    }
                }
            }
        }
    }
}
