node {
    try {
        stage ('Clone') {
            def repoUrl = checkout(scm).GIT_URL
	    def key = repoUrl.tokenize('/')[3]
	    def slug = repoUrl.tokenize('/')[4]
	    sh 'echo "The projectKey is: ${key}"'
	    sh 'echo "The repositorySlug is: ${slug}"'
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}  