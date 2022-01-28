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
	stages {
		stage("BUILD") {
			steps {
				echo "BUILD........."
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