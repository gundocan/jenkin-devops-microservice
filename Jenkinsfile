pipeline{
	agent any
	//agent{docker{image 'maven:3.6.3'}}
	//agent{docker{image 'node:13.8'}}
	environment{
		dockerHome = tool 'mydocker'
		mavenHome = tool 'mymaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}

	stages{

		stage('Build'){
			steps{
				//sh 'node --version'
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				echo " PATH-$PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
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
