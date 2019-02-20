pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                timeout(time: 3, unit: 'MINUTES') {
                sh 'date'
                sh '''
                    echo "Hello World"
                    echo "-------------------------------------------------"
                '''
                }
            }
        }
        stage('Deploy') {
            steps {
                sh 'date'
                sh '''
                    touch output.txt
                    date >>output.txt
                '''
            }
        }   
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
