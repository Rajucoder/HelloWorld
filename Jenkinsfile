node {
    try {
        stage ('Clone') {
            def commitHash = checkout(scm).GIT_COMMIT
            sh "echo 'Commit hash is: ${commitHash}'"
            println commitHash

            def repName = checkout(scm).repoName
            sh "echo 'Repository Name is: ${repName}'"
            println repName

            def rep = checkout(scm).repo
            sh "echo 'Repository is: ${rep}'"
            println rep

            def nm = checkout(scm).name
            sh "echo 'Name is: ${nm}'"
            println nm
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}  