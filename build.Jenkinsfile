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
                    echo "printing repo properties"
                    echo "name: $repository.name"
                    echo "owner: $repository.owner"
                    echo "defaultBranch: $repository.defaultBranch"
                    echo "description: $repository.description"
                    echo "url: $repository.url"
                    echo "cloneUrl: $repository.cloneUrl"
                    echo "sshUrl: $repository.sshUrl"
                    echo "gitUrl: $repository.gitUrl"
                    echo "private: ${repository.isPrivate()}"
                    echo "fork: $repository.fork"
                    echo "stargazersCount: $repository.stargazersCount"
                    echo "forksCount: $repository.forksCount"
                    echo "openIssuesCount: $repository.openIssuesCount"
                    echo "id: $repository.id"
                }
            }
        }
    }
}
