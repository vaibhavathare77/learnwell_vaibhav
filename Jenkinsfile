pipeline {
    agent any
	environment {
        surname = "Palase"
        firstname = "Krishana"
        }
    stages {
        stage('No-op') {
            steps {
                sh 'ls'
                sh '''
                echo "for pull"
                echo "BUILD_URL"
                echo "${BUILD_URL}"
                echo "BUILD_TAG"
                echo "${BUILD_TAG}"
                echo "BUILD_NUMBER"
                echo "${BUILD_NUMBER}"
                echo "BUILD_ID"
                echo "${BUILD_ID}"
                echo "JOB_NAME"
                echo "${JOB_NAME}"
                echo "JOB_URL"
                echo "${JOB_URL}"
                '''
            }
        }
        stage ("Input_Echo") {		//an arbitrary stage name
            steps {
			    input(message: "Should we continue?", ok: "Yes, we should.")
            }
		}
        stage ("Run_Echo") {		//an arbitrary stage name
            steps {
                  build job: 'Echo', parameters: [string(name: 'surname', value: surname)]
            }
        }
        stage ("Input_String_Echo") {		//an arbitrary stage name
            steps {
			    input(message: "Should we continue?", ok: "Yes, we should.")
			}
		}
		stage ("Run_String_Echo") {		//an arbitrary stage name
            steps {
//                build job: 'String_Echo', parameters: [$class: 'IntegerParameterValue', name: 'surname', defaultValue: 'Athare', description: 'please provide surname']
                  build job: 'String_Echo', parameters: [string(name: 'surname', value: surname), string(name: 'firstname', value: firstname)]
            }
        }
    }
}
