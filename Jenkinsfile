pipeline {
    agent any
    stages {
        stage('No-op') {
            steps {
                sh 'ls'
                sh '''
                echo "Build url"
                echo "${BUILD_URL}"
                '''
            }
        }
    }
    post {
    success {
        mail to: 'vaibhavathare77@gmail.com',
             subject: "Failed Pipeline:",
             body: "Something is wrong with"
    }
}
}
