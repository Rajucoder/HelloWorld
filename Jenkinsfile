pipeline{
	agent any
	stages{
		stage('preparation'){
			steps{
				echo "Build preparation"
				checkout scm
			}
		}
		stage('Auto Tagging'){
			steps{
				echo "Tagging"
			}
		}
	}
}
