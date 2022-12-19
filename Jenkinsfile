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