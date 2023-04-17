pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // build your application here
            }
        }
    }
    
    post {
        always {
            // send email notification
            mail to: 'email@example.com',
                 subject: "Build ${env.JOB_NAME} ${env.BUILD_NUMBER} ${currentBuild.result}",
                 body: "Build ${env.JOB_NAME} ${env.BUILD_NUMBER} ${currentBuild.result} has completed."
            
            // send Slack notification
            slackSend channel: '#général',
                      message: "Build ${env.JOB_NAME} ${env.BUILD_NUMBER} ${currentBuild.result} has completed."
        }
    }
}
