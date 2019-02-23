pipeline {
    agent any
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
    }
}
