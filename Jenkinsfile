pipeline {
 agent any
 stages{
  stage ('Exemple'){
   steps{
    echo 'Hello World'
   }
  }
 }
 post{
  always{
   slackSend channel: 'exercice', color: '#00ff00', message: 'Testing Jekins with Slack', tokenCredentialId:'slack-id'
  }
 }
}
