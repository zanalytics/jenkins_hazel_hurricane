pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
                slackSend color: '#BADA55', message: 'Hazel Hurricane is Started!!!'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            slackSend color: '#BADA55', message: 'Hazel Hurricane is finished!!!'
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
