stage('Checkout/Tag'){
	node{
		cleanWs()
		withCredentials([usernamePassword(credentialsId: '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',
		usernameVariable:'', passwordVariable: 'Token')]){
			sh """
			 curl --data '{
					"tag_name": "1.0.0",
					"target_commitish": "main",
					"name": "Release 1.0.0",
					"body": "Release of version",
					"draft": false,
					"prerelease": false}' \
				https://github.com/api/v3/repos/Rajucoder/HelloWorld/releases?access_token=${Token} 
			"""
		}
	}
}