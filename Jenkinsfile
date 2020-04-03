node{
    stage('SCM Checkout'){
        git 'https://github.com/poojan007/my-app'
    }
    stage('Compile and Package'){
        sh "mvn package" 
    }
    stage('Email Notification'){
        mail bcc: '', body: '''Hi welcome to jenkins email alerts
        Thanks''', cc: '', from: 'crst@rma.org.bt', replyTo: '', subject: 'Jenkins Build', to: 'poojan.d.sharma@gmail.com'
    }
    stage('Slack Notification'){
        slackSend baseUrl: 'https://hooks.slack.com/services/', 
        channel: '#ditt-datahub', 
        color: 'good', 
        message: 'Hi this is poojan from jenkins!!!', 
        token: 'slack-token', 
        tokenCredentialId: 'slack-token'   
    }
}
