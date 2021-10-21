node {
    try {
        stage ('Clone') {
            def commitHash = checkout(scm).GIT_COMMIT
            bat "echo 'Commit hash is: ${commitHash}'"
            bat "git tag -a release"
	    bat "echo 'Tag create'"
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}  