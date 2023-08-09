def gv

pipeline {
	agent any
	parameters {
		string(name: 'VERSION', defaultValue: '', description: 'version to deploy on prod')
		choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
		booleanParam(name: 'executeTests', defaultValue: true, description:'')
	}

	environment {
        MY_VARIABLE = 'test pipeline script syntax'
    }
	stages { 
		stage("init") {
			steps {
				gv = load "script.groovy"
			}
		}
		
		stage("Env Variables"){
            steps{
                sh 'printenv'      
				sh "printenv"     				
            }
        }
		stage("build") {
				
			steps {
				echo "build the application .."
				echo "My variable value: ${env.MY_VARIABLE}"
			}
		}

		stage("test") {
			when {
				expression {
					params.executeTests
				}
			}
				
			steps {
				echo "test the application .."
			}
		}

		stage("desploy") {
				
			steps {
				echo "test the application .."
			}
		}	
	}
}