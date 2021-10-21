node {
    try {
        stage ('Clone') {
            def commitHash = checkout(scm).GIT_COMMIT
            bat "echo 'Commit hash is: ${commitHash}'"
            println commitHash
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}  