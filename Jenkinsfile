pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
        stage('slack-notification') {
            steps {
                slackSend(
                 color:  "good",
                 message: "<$JOB_URL|$JOB_NAME> ($currentBuild.currentResult): Build <$RUN_DISPLAY_URL|$BUILD_DISPLAY_NAME> ($currentBuild.durationString) : ",
                 baseUrl: "https://devops-ngp9932.slack.com/services/hooks/jenkins-ci",
                 channel: "général"
                 ) 
            }
        }
        stage('mail-notification') {
            steps {
                emailext(
                    subject: '$DEFAULT_SUBJECT', 
                    to: 'doc.kaddiri@com', 
                    body: 'test'
                )
            }
        }
    }
}
