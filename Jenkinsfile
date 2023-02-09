pipeline {
    agent none
    stages {
	
	stage('Non-Parallel Stage') {
		/*agent {
						label "Built-In"
		}*/
		
		steps{
				echo 'This stage will be executed first'
		}
	
	}
	
	
		stage('Run Tests'){
			parallel {
				stage('Test On Windows'){
					agent {
							label "Slave"
					}
					steps {
							echo 'task1 on Agent'
					}
				}
				stage('Test on Master'){
					/*agent{
						label "Built-In"
					}*/
					steps{
							echo 'Task1 on Master'
					}
				}
			}
			
		}
	
	}

}
