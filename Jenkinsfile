pipeline {
	agent any
		stages {
			stage('One'){
				steps{
					echo 'Hi canım'
				}
			}
			stage('Two'){
				steps{
					input('answer me')
				}
			}
			stage('Three'){
				when{
					not{
						branch "master"
					}
				}
				steps {
					echo 'Hello'
				}
			}
			stage('Four'){
				parallel{
					stage('Unit Test'){
						steps {
							echo "Running The Unit test"
						}
					}
					stage('Integration Test'){
						steps {
							echo 'Running the integration test'	
						}
					}	

				}
			}
				
		}
}
			
