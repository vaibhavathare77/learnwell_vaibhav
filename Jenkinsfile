pipeline {
    agent any
    stages {
        stage('No-op') {
            steps {
                sh 'ls'
                sh '''
                echo "Build url"
                echo "${BUILD_URL}"
                echo "${currentBuild.fullDisplayName}"
                '''
            }
        }
    }
}
