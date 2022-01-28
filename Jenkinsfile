// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Integration Test') {
// 		echo "Integration Test"
// 	}
// }

//SCRIPTED
// node {
// 	echo "BUILD"
// 	echo "TEST"
// 	echo "INTERGRATION TEST"
// }

//DECLARATIVE
pipeline {
	agent any
	// agent { docker { image 'maven:3.6.3'} }
	stages {
		stage("BUILD") {
			steps {
				// sh 'mvn --version'
				echo "BUILD........."
				echo "$PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
			}
		}

		stage("TEST") {
			steps {
				echo "TEST........."
			}
		}

		stage("INTEGRATION") {
			steps {
				echo "INTEGRATION.........."
			}
		}
	} 
	post {
		always {
			echo "ALWAYS OPTION"
		}
		success {
			echo "SUCCESS OPTION"
		}
		failure {
			echo "FAILURE OPTION"
		}
	}
}