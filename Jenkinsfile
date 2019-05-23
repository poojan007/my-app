node{
    stage('SCM Checkout'){
        git 'https://github.com/poojan007/my-app'
    }
    stage('Compile and Package'){
        def mvnHome = tool name: 'maven-3', type: 'maven'
        sh "${mvnHome}/bin/mvn package" 
    }
    stage('Email Notification'){
        mail bcc: '', body: '''Hi welcome to jenkins email alerts
        Thanks''', cc: '', from: 'crst@rma.org.bt', replyTo: '', subject: 'Jenkins Build', to: 'poojan.d.sharma@gmail.com'
    }
}
