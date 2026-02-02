/* groovylint-disable CompileStatic, NestedBlockDepth */

pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                script {
                    sh 'printenv'
                    if (env.CHANGE_ID) {
                        echo "change ID: ${env.CHANGE_ID}"
                    } else {
                        echo 'no change ID!'
                    }
                }
            }
        }
    }
}
