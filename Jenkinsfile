pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
    }
    post {
        success { gerritReview score:1 }
        failure { gerritReview score:-1 }
    }
}
