pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    build 'PES1UG22CS382-1'
                    sh 'g++ -o randomfile PES1UG22CS382.cpp' 
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './randomfile'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }

    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
