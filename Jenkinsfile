//scripted
// node {
// 	echo "Build"
// 	echo "Test"
// 	echo "Integration Test"
// }

//Declarative 
pipeline{
	agent any
	// agent { docker { image 'maven:3.6.3' } }
	environment{
		dockerHome=tool 'myDocker'
		mavenHome=tool 'myMaven'
		path="$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				
			}
		}
		stage('Test'){
			steps{
				
				echo "Test"
				echo "BUILD_ID-$env.BUILD_ID"
				echo "JOB_NAME-$env.JOB_NAME"
				echo "BUILD_URL-$env.BUILD_URL"
				echo "JOB_URL-$env.JOB_URL"
			}
		}
		stage('Integration Test'){
			steps{
				
				echo "Integration Test"
			}
		}
	}
	post{
		always{
			echo "I am awesome"
		}
		success{
			echo "success"
		}
		failure{
			echo "fail"
		}
	}
}