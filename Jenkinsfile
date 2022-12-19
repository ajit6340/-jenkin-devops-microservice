//scripted
// node {
// 	echo "Build"
// 	echo "Test"
// 	echo "Integration Test"
// }

//Declarative 
pipeline{
	agent {docker {image 'python:3.12-rc-bullseye'}}
	stages{
		stage('Build'){
			steps{
				sh 'python --version'
				echo "Build"
				
			}
		}
		stage('Test'){
			steps{
				
				echo "Test"
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