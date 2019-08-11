pipeline {
	agent any 
	environment {
		username = 'jithender'
	}
	stages {
		stage('stage 1'){
			steps {
				writeFile file: 'groovy1.txt', text: "hello Mr.${username}"
				sh 'ls -l groovy1.txt'
				sh 'cat groovy1.txt'
			}
		}
	}
}
