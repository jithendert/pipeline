pipeline {
	agent any 
	
	stages {
		stage('stage 1'){
			environment {
				username = 'jithender'
			}
			steps {
				writeFile file: 'groovy1.txt', text: "hello Mr.${username}"
				sh 'ls -l groovy1.txt'
				sh 'cat groovy1.txt'
			}
		}
	}
}
