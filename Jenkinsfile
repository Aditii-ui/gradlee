pipeline{
	agent any
	tools{
		gradle 'Gradle'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch:'master', url:'https://github.com/Aditii-ui/gradlee.git'
			}
		}
		stage('Build'){
			steps{
				sh 'gradle build'
			}
		}
		stage('Test'){
			steps{
				sh 'gradle test'
			}
		}
		stage('Run'){
			steps{
				sh 'gradle run'
			}
		}
	}
	post{
		success{
			echo 'Build and Deployment successfull'
		}
		failure{
			echo 'Build failed!'
		}
	}
}
