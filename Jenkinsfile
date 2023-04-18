pipeline {
 agent any
 stages{
  stage ('Exemple'){
   steps{
    echo 'Hello World'
   }
  }
  stage('mail-notification')
   steps {
    emailext(
     subject: '$DEFAULT_SUBJECT',
     to: 'doc.kaddiri@gmail.com',
     body: 'test'
    )
   }
 }
}
 post{
  always{
   slackSend channel: 'exercice', color: '#00ff00', message: 'Testing Jekins with Slack', tokenCredentialId:'slack-id'
  }
 }
}
