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
		stage('stage 2'){
			
			steps {
				timeout(time: 3, unit: 'MINUTES') {
					retry(5) {
						sh 'echo deploying ${company}'
					}
				}
				sleep 60
				echo "hello mr.${env.username}"
			}
		}
	}
}
