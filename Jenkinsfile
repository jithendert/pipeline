pipeline {
	agent any 
	stages {
		stage('stage 1'){
			steps {
				echo 'hello world'
				powershell label: '', script: 'touch /test.txt'
			}
		}
	}
}
