pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo date'
                sh '''
                    echo "Hello World"
                    echo "-------------------------------------------------"
                '''
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "date'
                sh '''
                    touch output.txt
                    date >>output.txt
                '''
            }
    }
}
