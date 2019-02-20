pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'date'
                sh '''
                    echo "Hello World"
                    echo "-------------------------------------------------"
                '''
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
}
