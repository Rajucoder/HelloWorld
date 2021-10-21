node {
    try {
        stage ('Clone') {
            def commitHash = checkout(scm).GIT_COMMIT
            bat "echo 'Commit hash is: ${commitHash}'"
            println commitHash

            def repName = checkout(scm).repoName
            bat "echo 'Repository Name is: ${repName}'"
            println repName

            def rep = checkout(scm).repo
            bat "echo 'Repository is: ${rep}'"
            println rep

            def nm = checkout(scm).name
            bat "echo 'Name is: ${nm}'"
            println nm
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}  