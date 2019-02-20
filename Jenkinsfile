pipeline {
    agent any
    stages {
        stage('No-op') {
            steps {
                sh 'ls'
                sh '''
                echo "${currentBuild.fullDisplayName}"
                echo "${env.BUILD_URL}"
                '''
            }
        }
    }
    post {
    success {
        mail to: 'vaibhavathare77@gmail.com',
             subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
             body: "Something is wrong with ${env.BUILD_URL}"
    }
}
}
