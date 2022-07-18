pipeline{
	agent any
	stages{

		stage('Build'){
			steps{
				echo "Build"

			}
		}
		stage('Test'){
			steps{
				echo "Test"

			}
		}
		stage('Integration test'){
			steps{
				echo "Integration test"

			}
		}
	} 
	post {
		always{
			echo 'Im awesome I run always'
		}
		success{
			echo 'Im run when you are successful'
		}
		failure{
			echo 'Im run when you fail'
		}
	}

	
}
