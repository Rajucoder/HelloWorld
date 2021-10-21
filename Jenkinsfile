node {
    try {
        stage ('Clone') {
	withCredentials([gitUsernamePassword(credentialsId: 'Raju', gitToolName: 'Default')]) {
    		sh(\"\"\"#!/bin/bash -xl
                                             git config --global user.email "rajeshwarinadar721@gmail.com"
                                             git config --global user.name "Rajucoder"
                                             git clone --branch main https://github.com/Rajucoder/HelloWorld.git
                                             cd HelloWorld
                                             echo "Creating new Tag"
                                             git tag -a release -m "Release Candidate"
                                             git push origin release
                                             echo "Tag pushed to remote"
                                          \"\"\".stripIndent())
	}
        def repoUrl = checkout(scm).GIT_URL
	def key = repoUrl.tokenize('/')[3]
	def slug = repoUrl.tokenize('/')[4]
	echo "The projectKey is: ${key}"
	echo "The repositorySlug is: ${slug}" 
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}  
