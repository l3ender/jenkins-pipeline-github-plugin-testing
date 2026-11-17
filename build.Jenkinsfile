/* groovylint-disable CompileStatic, NestedBlockDepth */

pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                script {
                    echo "printing repo properties"
                    def repo = repository
                    echo "name: $repo.name"
                    echo "owner: $repo.owner"
                    echo "defaultBranch: $repo.defaultBranch"
                    echo "description: $repo.description"
                    echo "htmlUrl: $repo.htmlUrl"
                    echo "cloneUrl: $repo.cloneUrl"
                    echo "sshUrl: $repo.sshUrl"
                    echo "gitUrl: $repo.gitUrl"
                    echo "private: ${repo.isPrivate()}"
                    echo "fork: $repo.fork"
                    echo "id: $repo.id"
                }
            }
        }
    }
}
