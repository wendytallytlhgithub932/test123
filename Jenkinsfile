pipeline {
  //  agent any
agent {
		node {

			label 'Agent Test Agent 1'
		}
}	
    environment {
        NEW_VERSION = "1.3.0"
    }
	stages { 
		stage("build") {		
          steps {
          		echo "building the application"
              echo "building version ${NEW_VERSION}"
        		}
		}

		stage("test") {
            when {
                expression {
                BRANCH_NAME == 'dev' 
                }
            }			
            steps {
          		echo "Testing step the application"
        	}
		}

		stage("desploy") {
				
			steps {
          		echo "Testing step the application"
        		}
		}	
	}
}
