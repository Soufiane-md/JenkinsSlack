pipeline {
    agent any
    stages{
        stage ('Exemple') {
            steps {
                echo 'Hello, the world'
                }
            }
        }
    post{
        always{
            slackSend channel: 'général', color: '#00ff00', message: 'Testing Jekins with Slack', tokenCredentialId: 'slack-id'
            }
        }
}
