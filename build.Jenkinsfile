/* groovylint-disable CompileStatic, NestedBlockDepth */

pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                script {
                    echo "printing repo properties"
                    echo "name: $repository.name"
                    echo "owner: $repository.owner"
                    echo "defaultBranch: $repository.defaultBranch"
                    echo "description: $repository.description"
                    echo "htmlUrl: $repository.htmlUrl"
                    echo "cloneUrl: $repository.cloneUrl"
                    echo "sshUrl: $repository.sshUrl"
                    echo "gitUrl: $repository.gitUrl"
                    echo "private: ${repository.isPrivate()}"
                    echo "fork: $repository.fork"
                    echo "id: $repository.id"
                }
            }
        }
    }
}
