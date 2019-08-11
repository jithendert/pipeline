pipeline {
	agent any 
	environment {
		username = "thota"
	}
	
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
		stage('stage 2'){
			
			steps {
				echo "hello mr.${username}"
			}
		}
	}
}
